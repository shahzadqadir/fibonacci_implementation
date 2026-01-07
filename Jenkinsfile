pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "pip install -r requirements.txt --break-system-packages"
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