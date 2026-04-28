pipeline {
    agent any
    
    parameters {
        // You can have multiple parameters here
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'Select version')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check to run tests')
    }
    
    environment {
        NEW_VERSION = '1.3.0'
    }
    
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
                echo "Building version ${params.VERSION}"
            }
        }

        stage('test') {
            when { 
                expression { params.executeTests == true } 
            }
            steps { 
                echo 'Testing Project' 
            }
        }
        
        stage('deploy') {
            steps {
                echo 'Deploying Project'
                echo "Deploying version ${params.VERSION}"
            }
        }
    }
}


Added Jenkins build step – Amna Ali (23i-2067)
