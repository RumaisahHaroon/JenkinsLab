pipeline {
    agent any
    
    tools {
        maven 'Maven3' 
    }
    
    environment {
        NEW_VERSION = '1.3.0'
    }

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run Tests?')
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                echo "Building version ${NEW_VERSION}"
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
            when { 
                expression { params.executeTests == true } 
            }
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
