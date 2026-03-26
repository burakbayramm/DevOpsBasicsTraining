pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '1', daysToKeepStr: '', numToKeepStr: '3')
    }
    stages {
      stage('Checkout') {
        steps {
          cleanWs()
          checkout scmGit(branches: [[name: 'march26']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/burakbayramm/DevOpsBasicsTraining.git']])
          sh 'ls -ltr'
        }
      }

  stage('Build') {
    steps {
      sh 'echo "my second stage"'
    }
  }

}
}