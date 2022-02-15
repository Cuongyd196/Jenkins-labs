pipeline {
    agent any

    environment {
        DOCKERHUB_CREDENTIALS=credentials('DockerHub')
        NAME = 'CUONG'
    }

    stages {
        stage('Init') {
            environment {
                STAGE1 = 'Init'
            }
            steps {
                echo "Init..."
                echo "STAGE: $STAGE1"
                telegramSend('Init job')
            }
        }
        stage('Build') {
            steps {
                echo "DOCKERHUB_CREDENTIALS_USR: $DOCKERHUB_CREDENTIALS_USR"
                echo "NAME: $NAME"
                echo "BUILD_ID : $BUILD_ID"
                echo "BUILD_URL : $BUILD_URL"
                telegramSend('Build - $PROJECT_NAME – # $BUILD_NUMBER – STATUS: $BUILD_STATUS!')
            }
        }
    }
}