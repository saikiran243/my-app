node('windows'){
   stage('SCM Checkout'){
     git 'https://github.com/saikiran243/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      //def mvnHome =  tool name: 'maven-3', type: 'maven'   
      bat 'mvn clean package'
   }
   stage('Email Notification'){
    mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      saikiran''', cc: '', from: 'saikiran181992@gmail.com', replyTo: 'saikiran.sd@gmail.com', subject: 'Jenkins Job', to: 'saikiran.sd@outlook.com'
  }
   //#stage('Slack Notification'){
     //  #slackSend baseUrl: 'https://hooks.slack.com/services/',
      // #channel: '#jenkins-pipeline-demo',
      // #color: 'good', 
       //#message: 'Welcome to Jenkins, Slack!', 
       //#teamDomain: 'javahomecloud',
       //#tokenCredentialId: 'slack-demo'
   //#}
}
