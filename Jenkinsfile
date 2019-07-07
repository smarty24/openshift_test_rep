pipeline {
    agent any 


    environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD @{upstream}").trim()
    }
    stages {
        stage('Build') { 
            steps {
                // 
                echo 'Build Stage'
                echo GET_BRANCH_NAME
                echo GIT_BRANCH

                script{
                    sh 'ls -l && git rev-parse --abbrev-ref HEAD'
                }
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