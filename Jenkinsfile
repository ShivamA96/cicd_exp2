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
                bat 'mvn clean package' // Execute Maven to clean and package the application using Windows command
            }
        }
        
        stage('Test') {
            steps {
                bat 'mvn test' // Execute Maven to run tests using Windows command
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
