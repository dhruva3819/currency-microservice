pipeline {
    agent {
        label 'java-slave'
    }

    tools {
        // Define tools if needed, e.g., JDK, Maven, etc.
    }

    parameters {
        string(name: 'APPLICATION_NAME', description: 'Enter your application name', defaultValue: 'i27app')
        booleanParam(name: 'RUN_TESTS', description: 'Would you like to run tests?', defaultValue: true)
        choice(name: 'ENV', description: 'Which environment should I be deploying to?', choices: ['DEV', 'TEST', 'PROD'])
        password(name: 'PASSWORD', description: 'Enter a password', defaultValue: 'SECRET')
    }

    stages {
        stage('Parameters Example') {
            steps {
                echo "My application name is: ${params.APPLICATION_NAME}"
                echo "Are tests running? ${params.RUN_TESTS}"
                echo "Deploying to: ${params.ENV}"
                echo "Password entered is: ${params.PASSWORD}"
            }
        }
    }
}
