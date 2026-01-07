pipeline {
    agent any
    stages {
        stage ("build") {
            steps {
                sh "echo building application."
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