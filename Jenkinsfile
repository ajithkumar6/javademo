pipeline {
    agent any
    environment {
         DOCKER_CRED=credentials('ajith_docker')
    }
    stages {
        stage('building image') {
            steps {
                sh 'docker build -t ajithkumar232/latest:$BUILD_NUMBER .'
            }
        }
   stage ('pushing ti dockerhub'){
     steps{
       sh 'docker login -u $DOCKER_CRED_USR -p $DOCKER_CRED_PSW'
       sh 'docker push ajithkumar232/latest:$BUILD_NUMBER'
     }
   }
 }
}
