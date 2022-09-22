pipeline {
    agent { label 'tomcat'}
    stages {
        stage ('compilation') {
            steps {
                sh 'echo Hello dear. this is a compilation'
            }
        }
        stage ('deployment') {
            steps {
               sh 'echo Hello dear. this is a deployment'
            }
        }
        stage ('finalize') {
            steps {
               sh 'echo Hello dear. this is a finalize'
            }
        }
        stage ('send mail') {
            steps {
               mail bcc: '', body: 'This build is successful', cc: '', from: '', replyTo: '', subject: 'This is building email', to: 'integrityking007@gmail.com'
            }
        }
     }    
} 
