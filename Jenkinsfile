pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat 'dir'
                bat 'echo Build successful - Login page is ready!'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '1.html', fingerprint: true
            }
        }
    }

    post {
        success { echo 'Pipeline completed successfully.' }
        failure { echo 'Pipeline failed.' }
    }
}
