pipeline {
  agent any

  tools {nodejs "Nodejs-16.14.0"}
  
  stages {
    stage("test") {
      steps {
        echo "testing the app"
      }
    }
    
    stage("build") {
      steps {
        // commented nodejs block because I'm using nodejs globally for all stages i.e. specified in tools block
//         nodejs('Nodejs-16.14.0') {
          sh 'cd ./client && npm install && cd ../server && npm run build:client'
//         }
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
