pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker image...'
                echo 'docker build -t jenkins-cicd-pipeline:latest .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo 'In production, this stage pushes the image to DockerHub and deploys it to a server.'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed — check console output above.'
        }
    }
}