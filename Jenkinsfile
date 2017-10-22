pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building.'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
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
}
