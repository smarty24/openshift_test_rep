pipeline {
    agent any 


    environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref").trim()
    }
    stages {
        stage('Darative: Checkout scm') { 
            steps {
                // 
                echo 'Build Stage'
                echo GIT_BRANCH
            }
        }
        stage('Build') { 
            steps {
                // 
                echo 'Build Stage'
                echo GET_BRANCH_NAME
            }
        }
        stage('Test') { 
            steps {
                // 
                echo 'Test Stage'
            }
        }
        stage('Deploy') { 
            steps {
                // 
                echo 'Deploy Stage'
            }
        }
    }
}