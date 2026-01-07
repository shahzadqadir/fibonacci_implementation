pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "pip install -r requirements.txt"
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