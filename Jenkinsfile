pipeline {

    agent {
        label 'windows'
    }

    environment {
        APP_NAME = 'MyApplication'
        VERSION = '1.0'
        ENVIRONMENT = 'DEV'
    }

    stages {

        stage('Build') {
            steps {
                bat 'echo Application: %APP_NAME%'
                bat 'echo Version: %VERSION%'
                bat 'echo Environment: %ENVIRONMENT%'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Testing %APP_NAME%'
                bat 'echo Running tests for version %VERSION%'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying %APP_NAME%'
                bat 'echo Deployment Environment: %ENVIRONMENT%'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
