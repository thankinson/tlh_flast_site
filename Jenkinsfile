pipeline {
    agent any

    stages {
        stage('Confirm Successfull GitPull') {
            steps {
                echo 'GitPull Success'
            }
        }
        stage('Docker Build'){
            steps {
                sh 'docker-compose up -d --build inital-setup-flask-app'
            }
        }
        stage('Check App is up'){
            steps {
                sh 'sleep 20'
                sh 'docker ps'
            }
        }

    }
}