pipeline {
    agent {
        node {
            label 'mde'
        } 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'package-manager-cli.bin install MOBILE-4.0'
                sh 'tizen build-native -a arm -c gcc -C Debug'
                sh 'cd Debug && tizen package -t tpk'
            }
        }
    }
}
