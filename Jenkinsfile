pipeline {
    agent {
        docker { image 'docker:latest' }
    }
    stages {
        stage('Example') {
            steps {
                sh 'docker build -t ajithkumar232/latest .'
            }
        }
    }
}
