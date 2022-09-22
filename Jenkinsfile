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
                sh 'sonar-scanner'
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
                sh 'cp .
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
