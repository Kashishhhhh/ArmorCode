pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/ArmorCode.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('hello-world-app')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d --name hello-world-container hello-world-app'
                }
            }
        }
    }
}

