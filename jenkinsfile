pipeline {
    agent any

    environment {
        DOCKERHUB_CREDENTIALS=credentials('DockerHub')
        NAME = 'CUONG'
    }

    stages {
        stage('Init') {
            steps {
                echo "Init..."
                telegramSend('Init job')
            }
        }
        stage('Build') {
            steps {
                echo "DOCKERHUB_CREDENTIALS_USR: $DOCKERHUB_CREDENTIALS_USR"
                echo "NAME: $NAME"
            }
        }
    }
}