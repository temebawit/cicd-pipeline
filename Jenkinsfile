pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/temebawit/cicd-pipeline.git', branch: 'main')
      }
    }


    stage('Who am I') {
        steps {
            sh 'whoami'
            }
        }


    stage('test') {
      steps {
        sh 'scripts/test.sh'
      }
    }

  }
}
