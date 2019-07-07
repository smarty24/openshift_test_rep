pipeline {
    agent any 

    script {
        GET_BRANCH_PATH = sh(returnStdout: true, script: 'pwd').trim()
    }
    environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "cd ${GET_BRANCH_PATH} && git rev-parse --abbrev-ref HEAD").trim()
    }
    stages {
        stage('Build') { 
            steps {
                // 
                echo 'Build Stage'
                echo GET_BRANCH_NAME
                script{
                    sh "pwd"
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