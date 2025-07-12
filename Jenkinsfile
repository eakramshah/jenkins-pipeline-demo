pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh '/opt/homebrew/bin/pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh '/opt/homebrew/bin/pytest test_app.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}

