pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/suoton/node.js-ci-cd-nginx.git'
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ssh -i to1.pem ec2-user@13.50.107.238  "cd /path/to/your/chat-app && npm start"'
            }
        }
    }
}
