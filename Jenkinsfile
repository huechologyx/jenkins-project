pipeline {
    agent any
    // options { skipDefaultCheckout()}
    // environment {
    //     IMAGE_NAME = 'sanjeevkt720/jenkins-flask-app'
    //     IMAGE_TAG = "${IMAGE_NAME}:${env.BUILD_NUMBER}"
    //     KUBECONFIG = credentials('kubeconfig-credentials-id')

    // }

    // environment {
    //     SERVER_CREDS=credentials('server-creds')
    // }

    stages {

                stage('setup') {
                    steps {

                        withCredentials([usernamePassword(credentialsId: 'server-creds', usernameVariable: "myuser", passwordVariable: "mypassword")]) {
                            sh '''
                            echo username: ${myuser}
                            echo password: ${mypassword}
                            '''
                        }
                        // echo "my creds: ${SERVER_CREDS}"
                        // echo "Username: ${SERVER_CREDS_USR}"
                        // echo "Password: ${SERVER_CREDS_PSW}"
                    }
                }

                stage('Test'){
                    steps {
                        sh 'pip3 --version'
                    }
                }

        // stage('Checkout') {
        //     steps {
        //         git url: 'https://github.com/huechologyx/jenkins-project.git', branch: 'main'
        //         sh "ls -ltr"
        //     }
        // }
        // stage('Setup') {
        //     steps {
        //        sh 'pip3 --version'
        //     }
        // }
        // stage('Test') {
        //     steps {
               
        //         sh "whoami"
        //     }
        // }
        // stage('Login to docker hub') {
        //     steps {
        //         withCredentials([string(credentialsId: 'dockerhubpwd', variable: 'dockerhubpwd')]) {
        //         sh 'echo ${dockerhubpwd} | docker login -u sanjeevkt720 --password-stdin'}
        //         echo 'Login successfully'
        //     }
        // }
        // stage('Build Docker Image')
        // {
        //     steps
        //     {
        //         sh 'docker build -t ${IMAGE_TAG} .'
        //         echo "Docker image build successfully"
        //         sh "docker images"
        //     }
        // }
        // stage('Push Docker Image')
        // {
        //     steps
        //     {
        //         sh 'docker push ${IMAGE_TAG}'
        //         echo "Docker image push successfully"
        //     }
        // }
        // stage('Deploy to EKS Cluster') {
        //     steps {
        //         sh "kubectl apply -f deployment.yaml"
        //         echo "Deployed to EKS Cluster"
        //     }
        // }
    }
}