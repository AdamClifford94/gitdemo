pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }
    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/AdamClifford94/gitdemo'
            }
        }
        stage('Test-Package') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Compile-Package') {
            steps {
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
        stage('install-Package') {
            steps {
                sh 'mvn install'
            }
        }        
    }
}
