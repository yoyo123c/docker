pipeline {
    parameters {
        choice (name: 'VERSION' , choices: ['1.1.0' , '1.2.0' , '1.3.0'])
        booleanParam (name: 'excuteTest' , defaultValue: true)
    }
    agent any

    stages {
        stage("Building Stage") {
            when {
                expression { params.excuteTest == true }
            }
            steps {
                echo 'Building the app'
            }
        }
        stage("Testing Stage") {
            steps {
                echo 'Testing the app'
            }
        }
        stage("Deploying Stage") {
            input {
                message "select your env"
                ok "done"
                parameters{
                    choice (name: 'ENV' , choices: ['windows' , 'linux' , 'other'])
                }
                
            }
            steps {
                echo "Deploying the app ${params.VERSION}"
                echo "Deploying the app ${params.ENV}"
            }
        }
    }
}
