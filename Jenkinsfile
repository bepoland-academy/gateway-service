pipeline {
  agent any
  stages {
    stage('Checkout Sources') {
      steps {
        git(url: 'https://github.com/bepoland-academy/gateway-service.git', branch: 'development')
      }
    }
    stage('Compile') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t pl.betse.beontime/gateway-service:latest .'
      }
    }
    stage('Push Docker Image') {
      steps {
        sh '''docker tag pl.betse.beontime/gateway-service:latest build-server:5000/pl.betse.beontime/gateway-service
docker push build-server:5000/pl.betse.beontime/gateway-service'''
      }
    }
  }
}