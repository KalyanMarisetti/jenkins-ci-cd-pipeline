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
                // [usernamePassword(credentialsId: 'yourCredentialId', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]
                withCredentials([usernamePassword( passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]) {
                        // sh 'sudo apt update'
                        // sh 'sudo apt install -y nodejs npm'
                        // sh 'npm --version'
                        // sh 'npm install'
                        // sh 'echo "Username: $USERNAME"'
                        // sh 'echo "Password: $PASSWORD"'
                        // sh 'npm test'
                    sh 'echo "kalyan@123: $PASSWORD"'
                    sh 'sudo apt install npm'
                    sh 'npm test'
                }

                // sh 'sudo apt install npm'
                // sh 'npm test'
            }
        }
        stage('Build'){
            steps{
                sh 'npm run build'
            }
        }
        //  stage('Build Image'){
        //     steps{
        //         // sh 'npm run build'
        //     }
        // }
    }
}