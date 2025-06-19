pipeline{
    agent any

    environment {
        BRANCH_NAME = 'master'
        GIT_URL = 'https://github.com/joygisela/aws-cicd.git'
    }
    stages{
        stage('git checkout'){
            steps{
                git branch: '${BRANCH_NAME}', url: '${GIT_URL}'
            }
           
        }
    }
   
}