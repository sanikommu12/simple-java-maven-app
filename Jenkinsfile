pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git(url: 'https://github.com/sanikommu12/simple-java-maven-app.git', branch: 'master', credentialsId: 'qwe1', poll: true)
      }
    }

    stage('Build') {
      steps {
        sh '/root/simple-java-maven-app/mvn clean package -Denforcer.skip=true'
      }
    }

  }
}