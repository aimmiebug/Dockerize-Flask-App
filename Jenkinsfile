pipeline {
    agent any

    stages {
        stage('Test Docker Access') {
            steps {
                echo 'Checking Docker access from Jenkins...'
                sh 'docker version'
                sh 'docker ps'
            }
        }
    }
}
