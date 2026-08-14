pipeline {

    agent {
        label 'windows'
    }

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['DEV', 'TEST', 'PROD'],
            description: 'Select deployment environment'
        )
    }

    stages {

        stage('Build') {
            steps {
                bat 'echo Building application...'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running tests...'
            }
        }

        stage('Deploy DEV') {
            when {
                expression {
                    params.ENVIRONMENT == 'DEV'
                }
            }

            steps {
                bat 'echo Deploying to DEV...'
            }
        }

        stage('Deploy TEST') {
            when {
                expression {
                    params.ENVIRONMENT == 'TEST'
                }
            }

            steps {
                bat 'echo Deploying to TEST...'
            }
        }

        stage('Deploy PROD') {
            when {
                expression {
                    params.ENVIRONMENT == 'PROD'
                }
            }

            steps {
                input message: 'Deploy to PROD?', ok: 'Deploy'

                bat 'echo Deploying to PROD...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
