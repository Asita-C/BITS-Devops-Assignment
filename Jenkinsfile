pipeline {
    agent any // Runs the pipeline on any available agent
   
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository
                git 'https://github.com/Asita-C/BITS-Devops-Assignment.git'
            }
        }
        
        stage('Build and Compile') {
            steps {
                // Your build and compile commands here
                sh 'mvn clean compile' // Example Maven build and compile command
            }
        }
    }
    
    post {
        always {
            // Cleanup steps if needed
            echo 'Pipeline execution completed!'
        }
        success {
            // Notification or further actions on success
            echo 'Build successful!'
        }
        failure {
            // Notification or further actions on failure
            echo 'Build failed!'
        }
    }
}
