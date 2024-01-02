pipeline {
    agent any

    tools {
        nodejs "Node"
    }

  

    stages {
        stage('Clean and Install Dependencies') {
            steps {
                bat 'npm cache clean --force'
                bat 'npm install --force'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Deploy in IIS') {
            steps {
                // Copy files using xcopy in Windows
                bat 'xcopy /Y C:\\Jaimin\\Text\\* C:\\Jaimin\\wwwroot\\TextUtils\\'
            }
        }
    }
}
