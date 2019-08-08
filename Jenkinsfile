pipeline {
    agent any
    stages {
        stage(' check out') {
            scm {
                git {
                    remote("${GITHUB_URL}")
                    branches('jenkins-with-docker-plugin')
                    extensions {
                        cleanAfterCheckout()

                    }
                }
            }
        }
        stage('config cloud') {
            steps {
                systemGroovyCommand(readFileFromWorkspace('add-docker-cloud.groovy')) {

                }
            }
        }
    }
}