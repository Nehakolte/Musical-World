pipeline {
    agent any
    environment {
        staging_server = "15.229.18.65"
    }
    stages {
        stage("Deploy to remote") {
            steps {
                sh "ssh -o StrictHostKeyChecking=no root@${env.staging_server} 'mkdir -p /var/www/html/Musical_World'"
                sh "scp -r ${WORKSPACE}/* root@${env.staging_server}:/var/www/html/Musical_World/"
            }
        }
    }
}
