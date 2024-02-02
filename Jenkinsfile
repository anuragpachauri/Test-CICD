pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Check out the code from GitHub
                    git 'https://github.com/anuragpachauri/Test-CICD.git'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Install Node.js dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Start your Node.js app
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

