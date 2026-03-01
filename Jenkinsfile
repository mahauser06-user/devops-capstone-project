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
                sh 'docker build -t maha006/devops-capstone-app .'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'maha006', passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $maha006 --Gooddayinternal1@'
                    sh 'docker push maha006/devops-capstone-app'
                }
            }
        }
    }
}
