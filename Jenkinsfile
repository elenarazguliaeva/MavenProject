pipeline {
    agent any
    tools {
        maven 'localmvn'
    }

    stages {
        stage('Build') {
            input {
                message "are you hungry?"
                ok "Yes"
                submitrer "lex,john"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Jenkins',
                           description: 'Description of question')
                }
            }
            steps {
                sh 'mvn --version'
                echo "Hello, ${PERSON}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                build job: 'checkstyle'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
