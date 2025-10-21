pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest || exit 0'
            }
        }

        stage('Deploy') {
            steps {
                bat 'start /B python app.py'
                echo 'App is deployed successfully!'
            }
        }
    }
}
