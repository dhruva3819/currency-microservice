pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        TODAYS_DAY = 'thursday'
    }

    stages {
        stage('buildstage') {
            when {
                environment name: 'TODAYS_DAY', value: 'thursday'
            }
            steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}

