pipeline {
    agent any
    tools { nodejs 'Node' }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                sh "pm2 start --name backend npm -- start"
                sh "pm2 list" // Add this line to check if PM2 processes are running
            }
        }
    }
}
