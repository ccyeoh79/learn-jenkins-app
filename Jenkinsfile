pipeline {
    agent any

    stages {
        stage('w/o Docker') {
            steps {
                sh 'echo "Wihtout Docker"'
            }
        }
        stage('w/ Docker') {
            agent {
                docker {
                    image 'node:23-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'echo "Wiht Docker"'
                sh 'npm --version'
            }
        }
    }
}
