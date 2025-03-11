pipeline {
    agent {
        docker {
            image 'node:14'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
