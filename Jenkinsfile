pipeline {
  agent any
  stages{
    stage('build'){
      steps{
        sh 'mvn clean install test package'
      }
    }
    stage('Testing') {
      steps {
        realtimeJUnit(testResults: '**/surefire-reports/**/*.xml')
      }
    }
  }
}
