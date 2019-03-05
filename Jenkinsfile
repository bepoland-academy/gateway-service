pipeline {
  agent any
  stages {
    stage('Checkout Sources') {
      steps {
        git(url: 'https://github.com/bepoland-academy/gateway-service.git', branch: 'development')
      }
    }
  }
}