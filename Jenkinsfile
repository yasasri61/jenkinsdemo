pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Started'
            }
        }

        stage('Test') {
            steps {
                bat 'if exist index.html echo Test Passed'
            }
        }

        stage('Deploy') {
            steps {
                bat 'xcopy * C:\\DeployFolder\\ /E /Y'
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful'
        }
    }
}