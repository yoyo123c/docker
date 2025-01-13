pipeline {
    agent any

    stages {
        stage("Building Stage") {
            when {
                expression { env.BRANCH_NAME?.trim() == 'patch-1' || env.BRANCH_NAME?.trim() == 'main' }
            }
            steps {
                echo "Current branch: ${env.BRANCH_NAME}"
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
                echo 'Deploying the app'
            }
        }
    }
}
