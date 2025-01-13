pipeline {

    agent any

    stages {
        stage("bulding stage") {
            steps {
               echo "Current branch: ${env.BRANCH_NAME}"
            }

           when {
                 expression { env.BRANCH_NAME == 'patch-1' || env.BRANCH_NAME == 'main' }
           }

                   
               
            }
            steps {
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
