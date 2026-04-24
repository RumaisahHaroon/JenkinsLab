pipeline {
    agent any
    environment {
        APP_VERSION = '1.0.0'
    }
stages {
stage('Build') {
steps {
echo 'Building..'
// Here you can define commands for your build
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
// Here you can define commands for your tests
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
// Here you can define commands for your deployment
}
}
}
}
