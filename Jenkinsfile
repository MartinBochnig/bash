pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './configure --prefix=/tmp/testroot'
                make
                make install
            }
        }
    }
} 
