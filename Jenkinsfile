pipeline {
    agent any

    tools {
        nodejs 'NodeJenkins'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }

       stage('Test') {
            steps {
                echo 'Integration Testing...'
                sh 'CI=true npm test -- --coverage'
            }
            post {
                always {
                    clover(cloverReportDir: 'coverage', cloverReportFileName: 'clover.xml',
                    healthyTarget: [methodCoverage: 70, conditionalCoverage: 80, statementCoverage: 80],
                    unhealthyTarget: [methodCoverage: 50, conditionalCoverage: 50, statementCoverage: 50],
                    failingTarget: [methodCoverage: 0, conditionalCoverage: 0, statementCoverage: 0],
                    )
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'npm run build'
            }
            post {
                always {
                   archiveArtifacts artifacts: 'build/**/*.*', onlyIfSuccessful: true
                }
            }
        }
    }
}