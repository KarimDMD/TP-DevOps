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
    }
}