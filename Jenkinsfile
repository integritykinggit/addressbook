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
