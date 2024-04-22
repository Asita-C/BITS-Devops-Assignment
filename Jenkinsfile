pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository
                git 'https://github.com/Asita-C/BITS-Devops-Assignment.git'
            }
        }
        
        stage('Build and Compile') {
            steps {
                script {
                    // Use Maven for build and compilation
                    withMaven(maven: 'MavenInstallationName') {
                        sh 'mvn clean compile'
                    }
                }
            }
        }
    }
    
    post {
        success {
            // Send a success notification (optional)
            echo 'Build and compilation succeeded!'
            // You can add additional steps like sending email notifications, etc.
        }
        
        failure {
            // Send a failure notification (optional)
            echo 'Build or compilation failed!'
            // You can add additional steps like sending email notifications, etc.
        }
    }
}
