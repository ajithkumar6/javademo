pipeline {
    agent {
        docker { image 'docker:latest'
                 label 'new'
    }
    }
    stages {
        stage('Example') {
            steps {
                sh 'docker build -t ajithkumar232/latest .'
            }
        }
    }
}
