pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git(
                    url: 'https://github.com/Kashishhhhh/ArmorCode.git',
                    branch: 'main'
                )
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
