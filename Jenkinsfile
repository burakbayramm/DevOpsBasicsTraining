pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '1', daysToKeepStr: '', numToKeepStr: '3')
    }
    stages {
      stage('stage1') {
        steps {
          sh 'echo "my first stage"'
        }
      }

  stage('stage2') {
    steps {
      sh 'echo "my second stage"'
    }
  }

}
}