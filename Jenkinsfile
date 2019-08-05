pipeline {
    agent none
    stages {
        stage('Container parallel') {
            parallel {
                stage('Container-1') {
                    agent {
                        docker {
                            image 'node:7-alpine'
                        }
                    }
                    steps {
                        sh 'node --version'
                    }
                }
                stage('Container-2') {
                    agent {
                        docker {
                            image 'nginx:mainline-alpine'
                        }
                    }
                    steps {
                        sh 'nginx -v'
                    }
                }
            }
        }
    }
}