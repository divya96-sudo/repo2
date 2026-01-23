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
                pwd()
            }
        }   
    }
}