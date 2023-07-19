pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh './mvnw clean compile'
      }
    }

  }
}