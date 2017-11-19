pipeline {
  agent any
  stages {
    stage('buildd') {
      steps {
        echo 'building'
      }
    }
    stage('ttest') {
      steps {
        timeout(time: 10) {
          echo 'ttest'
        }
        
      }
    }
  }
}