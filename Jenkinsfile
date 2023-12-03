pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {                
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }
        
        stage('Test') {
            steps {
                sh 'echo "No tests for HelloWorld"'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo "Deploying HelloWorld"'
                // Add deployment steps here
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded! Project built and deployed.'
        }
        failure {
            echo 'Pipeline failed! Check logs for details.'
        }
    }
}
