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
        stage ("deploy") {
            steps {
                script {
                    sh "git config --global user.email 'shahzadqadir@hotmail.co.uk' "
                    sh "git config --global user.name 'Shahzad Qadir' "
                    sh "git checkout main"
                    sh "git pull"
                    sh "git merge main origin/dev"
                }
            }
        }
    }
}