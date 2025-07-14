pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        TODAYS_DAY = 'wenseday'
    }

    stages {
        stage('buildstage') {
            when {
                environment name: 'TODAYS_DAY', value: 'thursday  '
            }
            steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}

