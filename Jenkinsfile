pipeline {
    agent any 

    environment {
        GET_BRANCH_NAME_1 = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
    }

    stages {
        
        stage('Build Master') { 
            steps {
                // 
                echo 'Build Stage'
                echo GIT_BRANCH_NAME
            }
        }
        stage('Test Master') { 
            steps {
                // 
                echo 'Test Stage'
                //echo GIT_BRANCH_NAME
            }
        }
        stage('Deploy Master') { 
            steps {
                // 
                echo 'Deploy Stage END'
                echo GET_BRANCH_NAME_1
            }
        }
    }
}