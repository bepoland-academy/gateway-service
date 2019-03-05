pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/bepoland-academy/users-service', branch: 'development')
        sh '''mvn clean install
docker build -t pl.betse.beontime/gateway-service:latest .
docker tag pl.betse.beontime/gateway-service:latest plato:5000/pl.betse.beontime/gateway-service
docker push http://plato:5000/pl.betse.beontime/gateway-service'''
      }
    }
  }
}