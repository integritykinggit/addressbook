pipeline {
    agent { label 'tomcat'}
    stages {
        stage ('compilation') {
            steps {
                sh 'mvn -B compile'
            }
        }
        stage ('static code analysis') {
            steps {
                sh '/home/ubuntu/sonar-scanner-4.7.0.2747-linux/bin/sonar-scanner'
            }
        }
        stage ('package') {
            steps {
                sh 'mvn -B package'
            }
        stage ('deploy tomcat') {
            steps {
                sh 'cp target/addressbook-2.0.war /var/lib/tomcat9/webapps/addressbook.war' 
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
