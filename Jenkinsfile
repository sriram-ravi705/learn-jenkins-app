pipeline {
    agent any

    stages {
        stage('build') {
            agent {
                docker {
                    image "node"
                }
            }
            steps {
                sh '''
                ls -lrt
                node --version
                npm --version
                npm run build
                ls -lrt
                '''
            }
        }
    }
}