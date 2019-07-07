pipeline {
    agent any 
<<<<<<< HEAD


    environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref @")
    }
=======
>>>>>>> 85ca6121cf7b790abbe9dc44b02ba65d2d8dbc70
    stages {
        stage('Set environment path') { 
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