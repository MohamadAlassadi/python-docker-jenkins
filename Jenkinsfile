pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the GitHub repository...'
                bat 'git --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                bat 'docker build -t github-python-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Running the Docker container...'
                bat 'docker run --rm github-python-app'
            }
        }
    }
}
