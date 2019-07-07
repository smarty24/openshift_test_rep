pipeline {
    agent any 

    environment {
        GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
    }
    stages {
        stage ('SCM checkout') {
            steps {
                            env.GET_BRANCH_NAME = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()

            }
        }
        stage('Build') { 
            steps {
                // 
                echo 'Build Stage'
                echo GET_BRANCH_NAME
                script{
                    sh "git show-ref --tags -d"
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