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
                sh "pytest ."
            }
        }
    }
}