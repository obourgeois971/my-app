node {
  stage('SCM Checkout') {
    git 'https://github.com/obourgeois971/my-app'
  }
  stage('Compile-Package') {
    // Get maven home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh '${mvnHome}/bin/mvn package'
  }
  stage('Email Notification') {
    mail bcc: '', body: '''Hi Welcom to Jenkins email alerts
    Thanks
    Oli''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'texmex430@gmail.com'
  }
  stage('Slack Notification') {
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
      channel: '#jenkins-pipeline-demo', 
      color: 'good',
      message: 'Welcom to jenkins, Slack!', 
      tokenCredentialId: 'slack-demo'
  }
}
