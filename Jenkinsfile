node {
  stage('SCM Checkout') {
    git 'https://github.com/obourgeois971/my-app'
  }
  stage('Compile-Package') {
    // Get maven home path
    def mvnHome = tool name: 'Maven 3', type: 'maven'
    sh '${mvnHome}/bin/mvn package'
  }
  stage('Email Notification') {
    mail bcc: '', body: '''Hi Welcom to Jenkins email alerts
    Thanks
    Oli''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'texmex430@gmail.com'
  }
}
