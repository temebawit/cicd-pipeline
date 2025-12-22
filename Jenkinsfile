pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/temebawit/cicd-pipeline.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        sh 'scripts/build.sh'
      }
    }

    stage('test') {
      steps {
        sh 'scripts/test.sh'
      }
    }

  }
}