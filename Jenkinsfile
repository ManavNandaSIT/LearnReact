pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from your version control system (e.g., Git)
                git  'https://github.com/ManavNandaSIT/LearnReact'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js and npm (Assuming you have Node.js and npm as dependencies)
                // Use a version manager like nvm if needed
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // Build the ReactJS project
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Run tests if you have them
                // sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the built ReactJS application
                // This could involve copying files to a server or any deployment process you follow
                // Example: rsync, SCP, etc.
            }
        }
    }

    post {
        success {
            // This block will be executed if the pipeline succeeds
            echo 'Build and deployment successful!'
        }
        failure {
            // This block will be executed if the pipeline fails
            echo 'Build or deployment failed. Please check the logs for details.'
        }
    }
}
