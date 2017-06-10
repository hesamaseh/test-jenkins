pipeline {
  agent {
    docker {
      image 'busybox'
    }
    
  }
  stages {
    stage('test') {
      steps {
        parallel(
          "test": {
            sh 'echo "test"'
            
          },
          "test 2": {
            sh 'echo "test 2"'
            
          },
          "test 3": {
            sh 'echo "test 3"'
            
          }
        )
      }
    }
    stage('build') {
      steps {
        sh 'echo "build"'
      }
    }
    stage('deploy') {
      steps {
        sh 'echo "deploy"'
      }
    }
    stage('verify') {
      steps {
        sh 'echo "verify"'
      }
    }
  }
}