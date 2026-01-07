pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "pip install pipenv --break-system-packages"
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