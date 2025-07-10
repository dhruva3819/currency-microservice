pipeline {
    agent {
        label 'java-slave' 
    }
    stages {
        stage('build') {
            steps {
                echo "Build stage from main branch"
            }
        }
        stage('Scans') {
            steps {
                echo "Scans stage from main branch"
            }
        }
        stage('dockerbuild') {
            steps {
                echo "Docker stage from main branch"
            }
        }
        stage('deployment') {
            steps {
                echo "Deploying stage from main branch"
            }
        }
    }
}
