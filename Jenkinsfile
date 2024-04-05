pipeline {
    agent any

    tools {
        nodejs 'NodeJenkins'
    }

    stages {
        stage('Preparation') {
            steps {
                echo 'Preparing...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
    }
}