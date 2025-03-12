pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/DevOpsAbhii/app.git'
            }
        }

        stage('Instalsasdasdasdasdl Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run  the Application') {
            steps {
                sh 'nohup node app.js &'
            }
        }
    }
}
