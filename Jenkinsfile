node{
    stage('SCM Checkout'){
    git 'https://github.com/Singh-Sandy/my-app_java_home_cloud.git'
    }
    stage('Compile-Package'){
    bat 'mvn package'
    }
    stage('Email Notification'){
    mail bcc: '', body: '''Hi welcome to the Jenkins email alerts
    Thanks & Regards
    Sandeep Singh''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'singh.sandi10@gmail.com'
    }
    stage('Slack Notificaiton'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
        channel: 'jenkins_pipeline_demo', 
        color: 'good', 
        message: 'Welcome to Jenkins, Slack!', 
        tokenCredentialId: 'slack-demo', 
        username: 'jenkins_pipeline_demo'
    }
}
