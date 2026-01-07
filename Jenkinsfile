pipeline {
    agent any
    stages {
        stage ("pre-build") {
            steps {
                sh "pip install -r requirements.txt --break-system-packages"
                sh "export PATH=$PATH:/var/jenkins_home/.local/bin"
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