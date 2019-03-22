pipeline {
    agent any
    stages {
        stage('CleanWS') {
            steps {
                echo 'Cleaning up /tmp/testroot'
                sh 'rm -Rf /tmp/testroot'
            }
        }
        stage('Configure') {
            steps {
                echo 'Running build automation'
                sh './configure --prefix=/tmp/testroot'
            }
        }
        stage('Build') {
            steps {
                sh 'make -f Makefile all -j8'
            }
        }
        stage('Install') {
            steps {
                sh 'make -f Makefile install'
            }
        }
    }
} 
