job('example-1') {
    scm {
        git {
            remote("${GITHUB_URL}")
            branches('jenkins-with-docker-plugin')
            extensions {
                cleanAfterCheckout()
                
            }
        }
    }
    steps {
        systemGroovyCommand(readFileFromWorkspace('add-docker-cloud.groovy')) {
            
        }
    }
}