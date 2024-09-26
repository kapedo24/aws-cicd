pipeline{
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL 'https://github.com/kapedo24/aws-cicd.git'
    }

    stages{
        stage('git checkout1'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t awscicd .'
                sh 'docker images'
            }
        }
    }
}