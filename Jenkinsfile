pipeline {
    agent any
    stages {
        stage ("setup") {
            steps {
                sh '''
                python3 -m venv .venv
                .venv/bin/python -m pip install -r requirements.txt
                '''
            }
        }
        stage ("test") {
            steps {
                sh ".venv/bin/python -m pytest ."
            }
        }
       
    }
}