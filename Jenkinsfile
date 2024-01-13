pipeline {
    agent any
    stages {
        stage('checkout'){
            steps{
                checkout scm
            }
        }
        stage('Test'){
            steps{
                sh 'sudo apt update'
                sh 'sudo apt install nodejs npm'
                sh 'npm test'
            }
        }
        stage('Build'){
            steps{
                sh 'npm run build'
            }
        }
    }
}