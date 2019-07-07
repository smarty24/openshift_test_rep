pipeline {
    agent any 
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
        stage('Build') { 
            steps {
                // 
                echo 'Build Stage'
                echo GIT_BRANCH_NAME
            }
        }
        stage('Test') { 
            steps {
                // 
                echo 'Test Stage'
                echo GIT_BRANCH_NAME
            }
        }
        stage('Deploy') { 
            steps {
                // 
                echo 'Deploy Stage END'
            }
        }
    }
}