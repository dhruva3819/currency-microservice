pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        TODAYS_DAY = 'monday'
    }

    stages {
        stage('buildstage') {
            when {
                environment name: 'TODAYS_DAY', value: 'monday'
            }
            when {
            expression { BRANCH_NAME: ==~ / (prod|hotfix)/ }
                        steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}
