pipeline {
    agent none

    stages {
        stage('build') {
            agent {
                docker {
                    image "node"
                }
            }
            steps {
                sh'''
                ls -lrt
                node --version
                npm --version
                npm ci
                npm run build
                ls -lrt
                '''
            }
        }
    }
}