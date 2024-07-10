pipeline {
    agent any
    environment {
        // define env varibales here
        MY_ENV_VAR = 'some value'
    }

    stages {
        stage('Checkout - Git Clone') {
            steps {
                git 'https://github.com/kennytoro/k8s_project1.git'
            }
        }

        stage('Build') {
            steps {
                // building of the src code
                sh '''
                ls
                echo 'built successfully'
                '''
            }
        }
    }
}
