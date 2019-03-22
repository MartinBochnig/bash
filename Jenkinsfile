pipeline {
    agent any
    stages {
        stage('Configure') {
            steps {
                echo 'Running build automation'
                sh './configure --prefix=/tmp/testroot'
            }
        }
        stage('Build') {
            steps {
                make '-f Makefile all -j8'
            }
        }
    }
} 
