pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "python3 -m venv .venv"
                sh "source .venv/bin/activate"
                sh "pip install -r requirements.txt"
            }
        }
        stage ("test") {
            steps {
                script {
                    sh "python3 -m pytest ."
                    echo "Tests successful."
                }
            }
        }
    }
}