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
     }    
} 
