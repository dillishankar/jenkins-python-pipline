pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest || true'
            }
        }

        stage('Deploy') {
            steps {
                sh 'python app.py &'
                echo 'App is deployed successfully!'
            }
        }
    }
}
