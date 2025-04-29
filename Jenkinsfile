pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'docker pull nginx'
            }
        }
        stage('remove existing container'){
            steps{
                sh 'docker stop hello || true'
                 sh 'docker rm hello || true'
                 sh 'docker run -it -d --name hello -p 8081:8000 nginx'
            }
        }
    }
}
