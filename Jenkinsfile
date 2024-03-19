pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Checkout the source code from your Git repository
                git 'https://github.com/amitpnd555/jenkins.git'

                // Install dependencies and build the Node.js app
                sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Run tests if applicable
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the Node.js app (this is just an example, adjust as needed)
                sh 'npm start'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed :('
        }
    }
}
