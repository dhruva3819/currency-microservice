pipeline {
    agent {
        label 'java-slave'
    }

    tools {

    }

//    enivroment {
// // ${ENV_NAME}
//    }

    parameters {
        string(name: 'APPICATION_NAME', description: 'enter your application nmae', defaultvalues: 'i27app')
        booleanparam(_name: 'RUN_TESTS', DESCRIPTION: 'would you like to run ?',defaultvalue: true)
        choice(name:'ENV', description: 'WHICH ENV SHOULD I BE DEPOLYING ?', CHOICES: ['DEV', 'TEST', 'prod'])
        pasword(name: 'PASSWORD', description: 'Enter a password', defaultvalue: 'SECRECT')
    }
    stages {
        satge ('parametersEample'){
            steps {
                // code 
                echo "my application name is : ${params.APPLICATION_NAME}"
                echo "are testing running ? ${params.RUN_TESTS}"
                echo "Depolying to ***** ${params.ENV}"
                echo "Password Entered is: ${params.PASSWORD}"
            }
        }
    }
}
