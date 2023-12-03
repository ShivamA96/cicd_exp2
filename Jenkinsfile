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
                sh 'mvn clean package' // Execute Maven to clean and package the application
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test' // Execute Maven to run tests
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
