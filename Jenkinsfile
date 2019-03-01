pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/bepoland-academy/users-service', branch: 'development')
      }
    }
  }
}