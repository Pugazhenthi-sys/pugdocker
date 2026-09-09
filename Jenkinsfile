pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'YOUR_GITHUB_REPO_URL'
            }
        }

        stage('Check Docker') {
            steps {
                bat 'docker --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t factorial-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --rm factorial-app'
            }
        }
    }
}
