pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat './mvnw package'
      }
    }

    stage('Test') {
      steps {
        bat 'mvn test'
      }
    }

    stage('Package') {
      steps {
        bat 'mvn package'
      }
    }

    stage('Deploy') {
      steps {
        bat 'mvn deploy'
      }
    }

    stage('Email') {
      steps {
        emailext(subject: 'Build Passed!', body: 'Build Passed!', from: 'rswllee@hotmail.com', to: 'rswllee@hotmail.com')
      }
    }
    
  }
}
