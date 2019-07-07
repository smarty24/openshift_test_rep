pipeline {environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
    }
    agent any 


  
    stages {
        stage('Set Git path name') { 
            steps {
                // 
                script {
                    env.GIT_BRANCH_PATH=sh(returnStdout: true, script: "git name-rev --name-only HEAD").trim()
                    env.GIT_BRANCH_NAME=GIT_BRANCH_PATH.split('remotes/origin/')[1]
                    echo env.GIT_BRANCH_NAME
                }
                echo env.GIT_BRANCH_NAME
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