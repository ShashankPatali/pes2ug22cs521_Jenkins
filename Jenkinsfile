pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes2ug22cs521-1 main.cpp'
            }
        }
        
        stage('Test') {
            steps {
                sh './pes2ug22cs521-1'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
