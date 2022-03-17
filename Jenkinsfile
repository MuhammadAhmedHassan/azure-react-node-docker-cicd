pipeline {
  agent any

  stages {
    stage("test") {
      steps {
        echo "testing the app"
      }
    }
    
    stage("build") {
      steps {
        sh 'cd client'
        sh 'ls'
        echo '----------------------------------------------------'
        echo "building the app"
        script {
          def test = 2 + 2 > 3 ? 'cool' : 'not cool'
          echo test
        }
      }
    }
    stage("deploy") {
      steps {
        echo "deploying the app"
      }
    }
  }
}
