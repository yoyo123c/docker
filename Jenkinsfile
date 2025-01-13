pipeline {

    agent any

    stages {
        stage("bulding stage") {
            when {
                 expression { env.BRANCH_NAME == 'main' }
                   
               
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
}
