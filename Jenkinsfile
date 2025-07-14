pipeline {
    agent {
        label 'java-slave'
    }

    stages {
        stage('build') {
            steps {
                echo "************ Building the application ************"
            }
        }

        stage('sonar') {
            steps {
                echo "************ Performing the sonar scans ************"
            }
        }

        stage('dockerbuild') {
            steps {
                echo "************ Building docker image ************"
            }
        }

        stage('deployToDevEnv') {
            steps {
                echo "************ Deploying to dev environment ************"
            }
        }

        stage('deployToTestEnv') {
            steps {
                echo "************ Deploying to test environment ************"
            }
        }

        stage('deployToStageEnv') {
            when {
                branch 'release/*'
            }
            steps {
                echo "************ Deploying to stage environment ************"
            }
        }

        stage('deployToProdEnv') {
            when {
                tag pattern: "v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "************ Deploying to production environment ************"
            }
        }
    }
}
