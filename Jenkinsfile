pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=petclinic \\
  -Dsonar.projectName=\'petclinic\' \\
  -Dsonar.host.url=http://13.235.54.227:9000 \\
  -Dsonar.token=sqp_430bd009cf83ea948e8b19d1b0db414c26411a49'''
      }
    }

  }
}