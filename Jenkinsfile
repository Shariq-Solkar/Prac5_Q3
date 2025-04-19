pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Mariyanaaz/DO_Practical_5.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dir('Q3') {
                        docker.build('java-hello-world-app', '.')
                    }
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('java-hello-world-app').run()
                }
            }
        }
    }
}
