pipeline {

    agent any

    stages {
        stage("bulding stage") {
            steps {
               echo "Current branch: ${env.BRANCH_NAME}"
            }

            when {
              expression { env.BRANCH_NAME.trim() == 'patch-1' || env.BRANCH_NAME.trim() == 'main' }
            }
            
                echo 'bulding the app'
            }
        }
         stage("testing stage") {
            steps {
                echo 'testing the app'
            }
        }
             stage("deploying stage") {
                steps {
                   echo 'deploying the app'
        }
     }
   }
