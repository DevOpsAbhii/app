pipeline {
    agent any
    environment {
        NODEJS_HOME = '/usr/bin'  // Path to Node.js
    }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/DevOpsAbhii/app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'node app.js &'
            }
        }
    }
}
