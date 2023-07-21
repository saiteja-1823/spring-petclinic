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
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://172.31.18.185:9000 \\
  -Dsonar.token=sqp_74b5a488773f5c5f4533dc9f781b8280f7236b82'''
      }
    }

  }
}