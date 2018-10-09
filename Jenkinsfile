pipeline {
  agent any
  stages {
    stage('SCM ') {
      steps {
        git(url: 'https://github.com/varma92/java.git', branch: 'master', credentialsId: 'git-cred')
      }
    }
    stage('Build step') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}