node{
   stage('SCM Checkout'){
     git 'https://github.com/murataltuntas401905/java-hello-world-with-maven.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven3', type: 'maven'
      sh "${mvnHome}/bin/mvn -v"
      sh "${mvnHome}/bin/mvn test"
   }
   stage('Email Notification'){
      //mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      //Thanks
      //Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'murat.altuntas401905@gmail.com'
      echo 'Email sent successfully...'
   }
   stage('Call Main Method'){
    sh "java -cp target/classes info.maigo.lab.hello.App"
   }
}
