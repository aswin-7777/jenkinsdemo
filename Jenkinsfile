pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m pytest'
            }
        }

        stage('Build') {
            steps {
                bat 'if exist build rmdir /s /q build'
                bat 'mkdir build'
                bat 'copy app.py build\\'
                bat 'copy requirements.txt build\\'
            }
        }
    }
}