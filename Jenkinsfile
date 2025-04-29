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
                sh 'docker rm -f app || true'
            }
        }
         stage('run the container') {
            steps {
                sh 'docker run -it -d --name app -p 80:8000 nginx'
            }
        }
    }
}
