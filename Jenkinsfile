pipeline {
    agent any
    environment {
         DOCKER_CRED=credentials('ajith-docker')
    }
    stages {
        stage('building image') {
            steps {
                sh 'docker build -t ajithkumar232/latest:$BUILD_NUMBER .'
            }
        }
   stage ('pushing ti dockerhub'){
     steps{
       sh 'echo $DOCKER_CRED_PSW | docker login -u $DOCKER_CREDE_USR --password-stdin'
       sh 'docker push ajithkumar232/latest:$BUILD_NUMBER'
     }
   }
 }
}
