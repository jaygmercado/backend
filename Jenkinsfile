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
                // Your build steps here
                // For example, if it's a Node.js project:
                sh 'npm install'
                // Restart your backend or rebuild your frontend as needed
                // For example, if using pm2 for the backend:
                sh 'pm2 restart backend'
                }
            }
        }
    }
}
