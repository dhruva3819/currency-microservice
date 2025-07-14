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
                echo "Deploying to dev env"
            }
        }

        stage('prodDeploy') {
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

