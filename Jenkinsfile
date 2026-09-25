pipeline {
    agent any

    stages {

        stage('Create Virtual Environment') {
            steps {
                sh 'python3 -m venv .venv'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '.venv/bin/python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh '.venv/bin/python -m pytest'
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