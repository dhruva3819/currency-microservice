pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        DEPLOY_TO = 'production'
    }

    stages {
        stage('DeployToDev') {
            steps {
                echo "Deploying to dev environment"
            }
        }

        stage('DeployToProd') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "************ Deploying to production *******************"
            }
        }
    }
}
