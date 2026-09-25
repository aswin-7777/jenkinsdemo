pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }

        stage('Build') {
            steps {
                sh 'rm -rf build'
                sh 'mkdir build'
                sh 'cp app.py build/'
                sh 'cp requirements.txt build/'
            }
        }
    }
}