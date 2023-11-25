pipeline {
  agent {label "linux"}
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('build') {
      steps {
        sh '''
          tsc helloworld.ts
          node helloworld.js
        '''
      }
    }
  }
}