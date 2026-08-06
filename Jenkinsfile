pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Repository Checked Out'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }

    }

    post {
        always {
            echo 'Pipeline Finished'
        }

        success {
            echo 'Build Success'
        }

        failure {
            echo 'Build Failed'
        }
    }
}
