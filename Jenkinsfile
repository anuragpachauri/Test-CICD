pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        script {
          git 'https://github.com/anuragpachauri/Test-CICD.git'
        }

      }
    }

    stage('Build') {
      steps {
        script {
          sh 'npm install'
        }

      }
    }

    stage('Deploy') {
      steps {
        script {
          sh 'node app.js &'
        }

      }
    }

  }
  post {
    success {
      echo 'Node.js application deployed successfully!'
    }

    failure {
      echo 'Deployment failed!'
    }

  }
}