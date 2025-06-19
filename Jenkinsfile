pipeline{
    agent any

    environment {
        BRANCH_NAME = 'master'
        GIT_URL = 'https://github.com/joygisela/aws-cicd.git'
        IMAGE_TAG = 'joygisela/awscicd'
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }
    stages{
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
           
        }
        stage ('docker build') {
            steps {
                 sh 'docker build -t "{IMAGE_TAG}:${BUILD_NUMBER}" .'
                 sh 'docker images'
            }
           
        }
    }
   
}