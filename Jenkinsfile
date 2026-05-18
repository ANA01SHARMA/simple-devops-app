pipeline {
    agent any

    environment {
        PATH = "/home/anamika/.nvm/versions/node/v22.22.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'node -v'
                sh 'npm -v'
                sh 'npm install'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t simple-devops-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker stop simple-devops-container || true'
                sh 'docker rm simple-devops-container || true'
                sh 'docker run -d -p 3000:3000 --name simple-devops-container simple-devops-app'
            }
        }
    }
}
