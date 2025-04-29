pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'docker pull nginx'
            }
        }
         stage('run the container') {
            steps {
                sh 'docker run -it -d -p 80:8000 nginx'
            }
        }
    }
}
