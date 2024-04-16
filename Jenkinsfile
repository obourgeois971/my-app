node {
  stage('SCM Checkout') {
    git 'https://github.com/obourgeois971/my-app'
  }
  stage('Compile-Package') {
    // Get maven home path
    def mvnHome = tool name: 'Maven 3', type: 'maven'
    sh '${mvnHome}/bin/mvn package'
  }
}
