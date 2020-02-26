pipeline {
    agent none
    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/AdamClifford94/gitdemo'
                  }
            }
        stage('Test-Package') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn test'
            }
        }
        stage('Compile Package') {
            steps {
                sh "mvn clean"
                sh 'mvn package'
            }
        }
        stage('install-Package'){
            steps {
                sh 'mvn install'
            }
        } 
    }
}
