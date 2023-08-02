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
                sh "pm2 restart 0"
            }
        }
    }
}
