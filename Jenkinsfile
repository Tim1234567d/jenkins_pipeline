pipeline {
    agent any 
    environment {
        NEW_VERSION = "007"
    }
    stages {
        stage('Build') { 
            steps {
                echo "Build project"
                echo "building version ${NEW_VERSION}"
            }
        }
        stage('Unit-Test') { 
            when {
                expression {
                    BRANCH_NAME == "dev" || BRANCH_NAME == "main"
                }
            }
            steps {
                echo "Testing"
            }
        }
        stage('Deploy to dev') { 
            steps {
                echo "Deploy to dev"
            }
        }
        stage('Deploy to prod') { 
            steps {
                echo "Pipeline fineshed"
            }
        }
    }
    post { 
     always { 
        echo "post logic always"
     }
     success {
        echo "post logic success"
     }
   }
}

