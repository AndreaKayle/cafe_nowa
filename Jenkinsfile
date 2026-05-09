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
	stage('Deploy') {
    		steps {
        echo 'Simulating deployment...'
        sh 'echo App has been deployed!'
    }
}
    }
    post {
    success {
        mail to: 'youremail@gmail.com',
             subject: "BUILD SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
             body: "Build ${env.BUILD_URL} passed!"
    }
    failure {
        mail to: 'youremail@gmail.com',
             subject: "BUILD FAILED: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
             body: "Build failed. Check: ${env.BUILD_URL}"
    }
}