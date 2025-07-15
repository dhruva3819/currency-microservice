pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the application"
            }
        }

        stage('Parallel Scans') {
            parallel {
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

                stage('FinalScans') {
                    steps {
                        echo "Final Sonar Scan is executing"
                        sleep 15
                    }
                }
            }
        }
    }
}
