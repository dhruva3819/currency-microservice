pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo "Building the application"
            }
        }

        stage('SonarScans') {
            steps {
                echo "Sonar Scan is executing"
                sleep 15
            }
        }

        stage('FortifyScans') {
            steps {
                echo "Fortify Scan is executing"
                sleep 15
            }
        }

        stage('prismaScans') {
            steps {
                echo "Final prisma Scan is executing"
                sleep 15
            }
        }
    }
}
