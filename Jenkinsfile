pipeline {
    agent any
    environment {
        staging_server ="15.229.18.65"
    }
    stages {
        stage("Delpoy to remote") {
            steps {
            sh '''
                scp -r ${WORKSPACE}/* root@${staging_server}:/var/www/html/Musical_World/*'
            '''
            }
        }
        
    }
    
}
