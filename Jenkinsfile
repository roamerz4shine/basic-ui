pipeline {

    agent {
        docker {
            image 'dhsshine/tizen-studio:2.1'
            label 'docker'
        } 
    }

    stages {
        stage('Build') { 
            steps {
                sh 'echo hello'
                sh 'ls -alF'
            }
        }
    }
}
