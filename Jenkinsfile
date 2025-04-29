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
            }
        }
         stage('run the container') {
            steps {
                sh 'docker run -it -d --name hello -p 80:80 nginx'
            }
        }
    }
}
