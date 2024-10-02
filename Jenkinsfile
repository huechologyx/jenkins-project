pipeline {
    agent any

    options {
        timeout(time: 1, unit: 'MINUTES')
    }

    stages {

        stage('lint and format'){

                steps {
                    sh "sleep 70"
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

