pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                // Clone github repository
                git branch: 'main', url: 'https://github.com/Damian14349/Frontend.git'
            }
        }
                stage('Show files') {
            steps {
                // print files
                sh 'ls -la'
            }
        }
        stage('Run unit tests') {
            steps {
                // install requirements
                sh 'pip3 install -r requirements.txt'
                sh 'python3 -m pytest --cov=. --cov-report xml:test-results/coverage.xml --junitxml=test-results/pytest-report.xml'
            }
        }
    }
}
