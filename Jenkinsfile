pipeline {
    agent any
    
    tools {
        // Ensure this name matches Manage Jenkins -> Tools -> Maven
        maven 'M3' 
    }
    
    environment {
        NEW_VERSION = '1.3.0'
    }
    
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
                echo "Building version ${NEW_VERSION}"
                // Changed 'sh' to 'bat' for Windows
                bat "echo Installing dependencies..." 
            }
            
            post {
                always {
                    echo 'I will always run no matter what!'
                }
                success {
                    echo 'The build was successful!'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
