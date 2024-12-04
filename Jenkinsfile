pipeline {
    agent any

    stages {
        stage('clone repo') {
            steps {
                sh '''
                    git clone https://github.com/omarmohamed7i/docker.git
                '''
            }
        }
        stage('build') {
            steps {
                sh '''
                    cd docker 
                    docker build -t gad .
                    docker run -d -p 10000:80 gad
                '''
            }
        }
    }
}
