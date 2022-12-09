pipeline {
  agent any
  stages {
  stage('build') {
      steps {
        script {
          dir('springboot-backend') {
            sh "pwd"
            sh "mvn clean install"
            sh "mvn clean package"
          }
        }
      }
    }
  stage('test') {
      steps {
        script {
          dir('springboot-backend') {
            sh "mvn test"
          }
        }
      }
    }
  }
}
