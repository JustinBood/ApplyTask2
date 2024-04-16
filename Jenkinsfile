pipeline {
    agent any  // This tells Jenkins to run this pipeline on any available agent

    environment {
        HOME = '.'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checks out source code from version control
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            // Steps in this block will always be run, regardless of the pipeline's success or failure
            echo 'This will always run'
        }
        success {
            // Steps here will run only if the pipeline succeeds
            echo 'Success!'
        }
        failure {
            // Steps here will run only if the pipeline fails
            echo 'Failure!'
        }
    }
}
