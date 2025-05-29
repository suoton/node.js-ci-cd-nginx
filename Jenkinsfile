pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/suoton/node.js-ci-cd-nginx.git' // Clone your repository
                sh 'npm install' // Install dependencies
            }
        }
        stage('Deploy') {
            steps {
                sh 'ssh -i to1.pem ec2-user@13.50.107.238  "cd /home/ec2-user/chat-app && npm start"'
            }
        }
  
