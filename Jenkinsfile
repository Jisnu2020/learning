pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Jisnu2020/learning.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-cicd-app .'
            }
        }

        stage('Run App') {
            steps {
                sh 'docker run -d -p 5000:5000 flask-cicd-app'
            }
        }
    }
}