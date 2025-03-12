pipeline {
    agent any

    stages {
        stage('Checkout Code') {
	    steps {
		cleanWs() // Clears workspace
                checkout scm
            }

            steps {
                git 'https://github.com/DevOpsAbhii/app.git'
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

        stage('Deploy (Optional)') {
            steps {
                echo "Deployment steps go here"
            }
        }
    }

    post {
        success {
            echo "✅ Build Successful!"
        }
        failure {
            echo "❌ Build Failed!"
        }
    }
}
