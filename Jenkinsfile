pipeline {
    agent {
        docker {
            image 'python:3.12'
        }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'Application Build Successful'
            }
        }
    }
}