pipeline {
    agent any
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
         stage ('mail') {
            steps {
               mail bcc: '', body: 'This build is finished', cc: '', from: '', replyTo: '', subject: 'This is build mail', to: 'integrityking007@gmail.com'
            }
        }
    }
}
