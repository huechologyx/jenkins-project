pipeline {
 
agent any

    stages {
        stage('Setup') {
                steps {
                    echo "setup is being done"
                }
        }

          stage('Test') {
                steps {
                    echo "Test is being done"
                }
        }

        stage('Deploy'){

            input {
                message "Do you want to proceed further?"
                ok "Yes"
            }
            steps {
                echo "Running Deployment"
            }
        }



    }
}

