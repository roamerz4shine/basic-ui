pipeline {
    agent {
        node {
            label 'mde'
        } 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo hello'
                sh 'ls -alF'
                sh 'env'
                sh 'ls -alF /home/developer/tizen-studio/'
                sh 'package-manager-cli.bin install MOBILE-4.0'
                sh 'package-manager-cli.bin show-pkgs'
                sh 'tizen build-native -a arm -c gcc -C Debug'
                sh 'cd Debug && tizen package -t tpk'
            }
        }
    }
}
