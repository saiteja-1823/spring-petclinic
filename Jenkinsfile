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
  -Dsonar.host.url=http://172.31.43.211:9000 \\
  -Dsonar.token=sqp_006c6e02b258c54ca40db1d1ca99b8028abd3cf8'''
      }
    }

  }
}