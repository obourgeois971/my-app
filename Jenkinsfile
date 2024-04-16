node {
  stage('SCM Checkout') {
    git 'https://github.com/obourgeois971/my-app'
  }
  stage('Compile-Package') {
    sh 'mvn package'
  }
}
