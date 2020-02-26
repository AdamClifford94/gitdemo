node {
  stage('SCM Checkout'){
    git 'https://github.com/AdamClifford94/gitdemo'
  }
  stage('Test-Package'){
    sh 'mvn test'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
  
}
