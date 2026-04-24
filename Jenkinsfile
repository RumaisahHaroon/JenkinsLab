pipeline {
agent any
tools {
'Maven'
}
environment {
//variables defined here can be used by any stage
NEW_VERSION = '1.3.0'

}
stages {
stage('build') {
steps {
echo 'Building Project'
//using environment variable
//To output the value of variable in string use " "
echo "Building version ${NEW_VERSION}"
sh "nvm install"

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
