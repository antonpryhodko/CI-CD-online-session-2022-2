pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        script {
          checkout scm
          def customImage = docker.build("${registry}:${env.BUILD_ID}")
        }

      }
    }

  }
  environment {
    registry = 'vpanton/flask-app'
  }
}