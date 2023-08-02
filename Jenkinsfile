pipeline {
    agent any
    options {
        // Enable GitHub hook trigger for GITScm polling
        triggers { githubPush() }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'pm2 restart backend'
                }
            }
        }
    }
}
