pipeline {
  agent any
  stages {
    stage('Change Directory') {
      steps {
        dir(path: '/home/code')
      }
    }

    stage('error') {
      steps {
        sh '''sudo git pull https://github.com/anuragpachauri/Test-CICD.git
npm install -f
node app.js
'''
      }
    }

  }
}