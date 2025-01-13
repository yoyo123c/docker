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
            steps {
                echo "Deploying the app ${params.VERSION}"
            }
        }
    }
}
