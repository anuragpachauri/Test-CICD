pipeline {
  agent any
  stages {
    stage('Change Directory') {
      steps {
        dir(path: '/home/code')
      }
    }

    stage('') {
      steps {
        git(url: 'https://github.com/anuragpachauri/Test-CICD.git', branch: 'main')
        sh '''sudo git pull https://github.com/anuragpachauri/Test-CICD.git
npm install -f
node app.js
'''
      }
    }

  }
}