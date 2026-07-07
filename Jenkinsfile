pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Fetching source code from GitHub...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing Node.js dependencies...'
                bat 'npm install'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Node.js application...'
                bat 'node app.js'
            }
        }

        stage('Build Complete') {
            steps {
                echo 'Pipeline completed successfully!'
            }
        }

    }

    post {
        success {
            echo 'Build Status: SUCCESS'
        }

        failure {
            echo 'Build Status: FAILED'
        }
    }
}