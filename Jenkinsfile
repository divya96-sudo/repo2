pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', credentialsId: 'b89f5acf-4cbe-481e-ada6-7467f6e601db', url: 'https://github.com/divya96-sudo/repo2.git'
            }
        }

        stage('print current directory') {
            steps{
                echo "Current directory is: ${pwd()}"
            }
        }

        stage('build image') {
            sh '''docker build -t sample:latest .
            docker tag sam asia-south1-docker.pkg.dev/training-2024-batch/divya-repo/sam:latest
            docker push asia-south1-docker.pkg.dev/training-2024-batch/divya-repo/sam:latest'''
        }       
    }
}