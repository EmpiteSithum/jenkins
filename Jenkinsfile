pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building.'
                sh 'echo build number "$BUILD_NUMBER ${BUILD_NUMBER}"'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            steps {
              echo 'Deploying...'
            }
        }
    }
}
