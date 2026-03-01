pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/mahauser06-user/devops-capstone-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t maha006/devops-app .'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'maha006', passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $maha006 --Gooddayinternal1@'
                    sh 'docker push yourdockerhubusername/devops-app'
                }
            }
        }
    }
}
