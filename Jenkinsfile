pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Specify the dev branch
                    git branch: 'dev', url: 'https://github.com/suoton/node.js-ci-cd-nginx.git'
                }
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                // Stop any existing instance before starting a new one
                sh 'pkill -f app.js || true'
                sh 'nohup node app.js > app.log 2>&1 &'
            }
        }
    }
}
