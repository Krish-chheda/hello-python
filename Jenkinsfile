pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                    python3 -m pip install --upgrade pip
                    pip3 install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    pytest test_app.py -v
                '''
            }
        }

    }
}
