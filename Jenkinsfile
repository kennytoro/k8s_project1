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
        
        stage('Deploy') {
            steps {
                // deploying here
                echo "The Env variable is $MY_ENV_VAR"
                echo "kubectl apply -f ."
                echo " BUild id is $BUILD_ID"
            }
        }
    }
    post {
        success {
            // succefuly 
            echo 'Good job pipeline succeeded'
        }
        failure {
            echo ' Ooops opps failed we are outside'
        }
    }

}
