pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "pip install pipenv"
                sh "pipenv install --system"
            }
        }
        stage ("test") {
            steps {
                script {
                    sh "pytest ."
                    echo "Tests successful."
                }
            }
        }
    }
}