pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3025:3000 -p 5052:5000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
