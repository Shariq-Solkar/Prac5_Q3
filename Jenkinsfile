pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Shariq-Solkar/Prac5_Q3.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                dir('Q3') {
                    bat 'docker build -t java-hello-world-app .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --rm java-hello-world-app'
            }
        }
    }
}
