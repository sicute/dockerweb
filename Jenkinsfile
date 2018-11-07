pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'npm install'
                sh 'sudo npm install -g mocha'
                sh 'pm2 start server.js'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mocha' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
