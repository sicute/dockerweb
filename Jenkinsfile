pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                npm install
                sudo npm install -g mocha
                pm2 start server.js
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                mocha 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
