pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        echo 'Hello World'
        sh '''pipeline {
    agent any

    stages {
        stage(\'Build\') {
            steps {
                echo \'Building..\'
            }
        }

        stage(\'Test\') {
            steps {
                echo \'Testing..\'
            }
        }

        stage(\'Deploy\') {
            steps {
                echo \'Deploying....\'
            }
        }
    }
}'''
        }
      }

    }
    post {
      always {
        echo 'I will always say Hello again!'
      }

    }
  }