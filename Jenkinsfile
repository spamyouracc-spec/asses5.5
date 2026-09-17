pipeline {
    agent any

    environment {
        APP_NAME = 'RatetheBook'
        APP_VERSION = '2.1.0'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/spamyouracc-spec/asses5.5.git'
            }
        }

        stage('Show App Info') {
            steps {
                echo "Building ${env.APP_NAME}, version ${env.APP_VERSION}"
            }
        }

        stage('Build') {
            steps {
                bat 'python -m py_compile app.py'
                echo "${env.APP_NAME} version ${env.APP_VERSION} compiled successfully."
            }
        }
    }
}
