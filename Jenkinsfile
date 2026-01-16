pipeline {
    agent any

    environment {
        APP_NAME = 'MyApp'
        DEPLOY_ENV = 'main'
    }

    stages {
        stage('Build') {
            steps {
                echo "App name is ${APP_NAME}"
                echo "Deploying to environment: ${DEPLOY_ENV}"

                echo 'Building...'
                // Add build steps here
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                sh '''
                echo 'listing tools'
                which java || 
                which java || echo "Java not installed"
                which python3 || echo "Python not installed"
            '''


                // Add test steps here
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying...'
                echo "Deploying ${APP_NAME} to ${DEPLOY_ENV} environment"
                // Add deploy steps here
            }
        }
    }

}