pipeline {
    agent any

    stages {

        stage('Credential Test') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'e4c2a6c6-7b1e-4ddb-b3cf-d49016c78b05',
                        usernameVariable: 'MY_USER',
                        passwordVariable: 'MY_PASS'
                    )
                ]) {
                    echo "Username: ${MY_USER}"
                    echo "Password is protected"
                }
            }
        }
    }
}
