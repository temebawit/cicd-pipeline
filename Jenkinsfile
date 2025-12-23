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

     stage('Build Image') {
            steps {
                script {
                    // Билдим образ и сохраняем его в переменную 'app'
                    app = docker.build("tem212081/cicd-pipeline")
                    echo "image was successfully built"
                }
            }
        }

        stage('Push to Hub') {
            steps {
                script {
                    // 'docker_hub_creds_id' —  Credentials Jenkins
                    docker.withRegistry('https://registry.hub.docker.com', 'c7d0b75e-dfc7-4108-a4c6-b7dc0e5af483') {
                        
                        
                        app.push("${env.BUILD_NUMBER}")
                        
                       
                        app.push("latest")
                    }
                }
            }

    
  }
}}
