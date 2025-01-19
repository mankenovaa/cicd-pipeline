pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'aigerimimage'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/mankenovaa/cicd-pipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh './scripts/build.sh'
            }
        }

        stage('Test') {
            steps {
                sh './scripts/test.sh'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t mankenovaa/aigerimimage .'
            }
        }

    }
}
