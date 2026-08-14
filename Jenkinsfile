pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build v2 from GitHub'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!   sanj'
        }
    }
}
