pipeline {
    agent any

    environment {
        CREDENTIALS_ID ='d5462f29-66e0-4935-b915-0f80efdb82ab'
    }

    tools {
        nodejs 'node-tool'
    }

    stages {

        stage('Initialize') {
            steps {
                sh '''
                    npm install
                '''
            }
        }

        stage('Unit Tests') {
            steps {
                sh '''
                    npm run test -- --watchAll=false
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                    npm run build
                '''
            }
        }
    }
}