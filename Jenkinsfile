pipeline {
    agent any


    stages {

        stage('lint and format'){

                parallel {
                    stage('linting'){
                        steps {
                            sh "sleep 30"
                        }
                    }

                    stage('formatting'){
                        steps {
                            sh "sleep 30"
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

