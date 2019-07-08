pipeline {
    agent any 

    environment {
        GET_BRANCH_NAME_1 = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
    }

    stages {
        stage('Set path') { 
            steps {
                // 
                script {
                    env.GIT_BRANCH_PATH=sh(returnStdout: true, script: "git name-rev --name-only HEAD").trim()
                    env.GIT_BRANCH_NAME=GIT_BRANCH_PATH.split('remotes/origin/')[1]
                }
            }
        }
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
                echo GIT_BRANCH_NAME
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