pipeline {
    agent any 

    environment {
        BRANCH_NAME = 'main'
        GIT_URL  = 'https://github.com/Penda1604/aws-cicd2.git'
        IMAGE_TAG = "app1"  
        IMAGE_VERSION = ${BUILD_NUMBER}
      }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        
        stage('Docker Build') {
            steps {
                sh 'docker build -t ${IMAGE_TAG}:${IMAGE_VERSION} .'
                sh 'docker images'
            }
        }
    }
}
