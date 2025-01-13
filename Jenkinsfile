pipeline {
    parameters {
        choice (name: 'version' , choices: [ 1.1.0 , 1.2.0 , 1.3.0 ] , description: '')
        booleanParam (name: 'excutetest' , deafaultValue: true)
    }
    agent any

    stages {
        stage("Building Stage") {
            when {
                expression { param.excutetest == true }
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
            steps {
                echo 'Deploying the app ${param.version}'
            }
        }
    }
}
