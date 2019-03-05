pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/bepoland-academy/users-service', branch: 'development')
        sh 'mvn clean package dockerfile:tag dockerfile:push -Ddockerfile.repository=plato:5000'
      }
    }
  }
}