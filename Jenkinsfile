pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '1', daysToKeepStr: '', numToKeepStr: '3')
    }
    stages {
      stage('Checkout') {
        steps {
          cleanWs()
          sh 'echo "my first stage"'
        }
      }

  stage('Build') {
    steps {
      sh 'echo "my second stage"'
    }
  }

}
}