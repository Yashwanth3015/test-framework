pipeline {
    agent any

    stages {

        stage('Clone Code') {
         steps {
           git branch: 'main', url: 'https://github.com/Yashwanth3015/test-framework.git'
    }
}

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
          steps {
            bat 'python -m pytest tests'
    }
}

        stage('Generate Report') {
            steps {
                bat 'python -m pytest --html=reports/report.html'
            }
        }

    }
}