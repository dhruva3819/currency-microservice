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
                environment name: 'TODAYS_DAY', value: 'tuesday'
            }
            expression { BRANCH_NAME: ==~ / (prod/hotfix)/ }
                        steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}
