pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'docker pull nginx'
            }
        }
        stage('removing existing container'){
            steps{
                sh 'docker rm -f hello || true'
            }
        }
         stage('run the container') {
            steps {
                sh 'docker run -it -d --name hello -p 80:80 nginx'
            }
        }
    }
}
