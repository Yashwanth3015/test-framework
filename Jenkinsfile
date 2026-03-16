pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Yashwanth3015/test-framework.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest tests'
            }
        }

        stage('Generate Report') {
            steps {
                bat 'pytest --html=reports/report.html'
            }
        }

    }
}