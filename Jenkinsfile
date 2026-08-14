pipeline {
    agent {
        label 'windows'
    }

    stages {

        stage('Agent Test') {
            steps {
                bat 'whoami'
                bat 'hostname'
                bat 'echo Hello from Windows Agent'
            }
        }
    }
}
