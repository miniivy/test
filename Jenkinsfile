pipeline {
    agent any
 
    stages {
        stage('build') {
            steps {
                sh 'build check'
            }
        }
    }
 
    post {
        always {
            junit '**/target/*.xml'
        }
        failure {
            mail to:  junho@catenoid.net, subject: 'Pipeline fail email'
        }
    }
}
