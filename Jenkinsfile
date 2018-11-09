pipeline {
  agent any
  stages {
    stage('SCM ') {
      steps {
        git(url: 'https://github.com/varma92/java.git', branch: 'master', credentialsId: 'git-cred')
      }
    }
    stage('Tool Integration') {
      steps {
        tool(name: 'MVN', type: 'build tool')
        tool(name: 'JDK', type: 'java ')
      }
    }
    stage('Build ') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}