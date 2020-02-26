pipeline {
    agent none
    stages {
        stage('SCM Checkout') {
            git 'https://github.com/AdamClifford94/gitdemo'
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
           sh "mvn clean"
           sh 'mvn package'
        }
        stage('install-Package'){
        sh 'mvn install'
        } 
    }
}
