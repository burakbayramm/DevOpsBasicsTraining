pipeline {
    agent any
    parameters {
      string defaultValue: 'march26', description: 'Branch Name', name: 'checkout_branch'
    }
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '1', daysToKeepStr: '', numToKeepStr: '3')
    }
    stages {
      stage('Checkout') {
        steps {
          cleanWs()
          checkout scmGit(branches: [[name: "${params.checkout_branch}"]], extensions: [], userRemoteConfigs: [[url: 'https://github.com/burakbayramm/DevOpsBasicsTraining.git']])
          sh 'ls -ltr'
        }
      }

  stage('Build') {
    tools {maven 'maven-3.6.3'}
     steps {
      sh 'mvn clean package -DskipTests'
    }
  }

}
}