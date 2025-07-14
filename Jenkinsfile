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
                allOf {
                    environment name: 'TODAYS_DAY', value: 'tuesday'
                    expression {
                        return env.BRANCH_NAME ==~ /(prod|hotfix)/
                    }
                }
            }
            steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}
