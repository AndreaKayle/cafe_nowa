pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'echo Build step complete'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo Test step complete'
            }
        }
        stage('Archive') {
            steps {
                echo 'Archiving artifacts...'
                bat 'echo Archive step complete'
            }
        }
    }
    post {
        success { echo 'Pipeline completed successfully!' }
        failure { echo 'Pipeline FAILED!' }
    }
}