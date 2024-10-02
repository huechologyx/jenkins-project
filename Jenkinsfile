pipeline {
    agent any

parameters {
    string(name: 'ENVIRONMENT', defaultValue: 'dev', description: 'Specify the environment for development')
    booleanParams(name: 'RUN_TESTS', defaultValue: true, description: "Run Tests in pipeline")

}

    stages {
        stage('Test') {
            when {
                expression {
                    params.RUN_TESTS == true
                }
            }
            steps {
            echo "testing application"
            }
        }

        stage('Deploy'){
            steps {
                echo "deploying to ${params.ENVIRONMENT} environment"
            }
        }



    }
}

