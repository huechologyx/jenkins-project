pipeline {
    agent any


    stages {

        stage('lint and format'){

                stages {
                    stage('linting'){
                        steps {
                            echo "linting code in nested stage"
                        }
                    }

                    stage('formatting'){
                        steps {
                            echo "formatting code in nested stage"
                        }
                    }
                }

        }

                stage('setup') {
                    steps {

                        withCredentials([usernamePassword(credentialsId: 'server-creds', usernameVariable: "myuser", passwordVariable: "mypassword")]) {
                            sh '''
                            echo username: ${myuser}
                            echo password: ${mypassword}
                            '''
                        }

                    }
                }

                stage('Test'){
                    steps {
                        sh 'pip3 --version'
                    }
                }

    }
}

