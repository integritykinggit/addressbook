pipeline {
    agent { label 'tomcat'}
    stages {
        stage ('compilation') {
            steps {
  //              sh 'echo Hello dear. this is a compilation'
                sh 'mvn -B compile'
            }
        }
        stage ('static code analysis') {
            steps {
  //           sh 'echo Hello dear. this is a deployment'
                sh '/home/ubuntu/sonar-scanner-4.7.0.2747-linux/bin/sonar-scanner'
            }
        }
        stage ('package') {
            steps {
  //            sh 'echo Hello dear. this is a finalize'
                sh 'mvn -B package'
            }
        stage ('deploy tomcat') {
            steps {
 //              sh 'echo Hello dear. this is a finalize'
                sh 'cp ./target/addressbook-2.0.war var/lib/tomcat9/webapps/addressbook.war' 
            }
        }
     }
    post {
        failure {
            sh 'echo the build failed'
        }
        success {
            sh 'echo the build is successful'
        }
        always {
            sh 'echo the build is completed'
        }
    }
} 
