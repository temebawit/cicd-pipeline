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
        sh './scripts/build.sh'
      }
    }

    stage('test') {
      steps {
        sh './scripts/test.sh'
      }
    }

     stage('build docker image') {
      steps {
        sh 'docker build -t tem212081/cicd-pipeline .'
        echo 'image was successfully built'
      }
    }

    
  }
}
