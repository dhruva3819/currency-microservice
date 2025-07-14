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
                    environment name: 'TODAYS_DAY', value: 'monday'
                    expression {
                        return env.BRANCH_NAME ==~ /(prod|main)/
                    }
                }
            }
            steps {
                echo "Executing pipeline for 'when' condition example"
            }
        }
    }
}
