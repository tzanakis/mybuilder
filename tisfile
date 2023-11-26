pipeline {
  agent {label "linux"}
  tools {nodejs "node21"}
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