pipeline {
    agent {
        label 'java-slave' 
    }
    stages {
        stage('build') {
            steps {
                echo "Building the application"
            }
        }
        stage('Scans') {
            steps {
                echo "Perforing the sonar scans"
            }
        }
        stage('dockerbuild') {
            steps {
                echo "implementing the docker build"
            }
        }
        stage('devenv') {
            steps {
                echo "Deploying  to dev env"
                 }
        }
        stage('stageenv') {
            steps {
                echo "Deploying satge env"
                        }
        }
        stage('prodenv') {
            steps {
                echo "Deploying prod env"
            }
        }
    }
}

