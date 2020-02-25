node {
  stage('SCM Checkout'){
    git 'https://github.com/AdamClifford94/gitdemo'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
  
}
