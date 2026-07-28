pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                sh 'python3 --version'
                sh 'pip3 --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'Application Build Successful'
            }
        }
    }
}