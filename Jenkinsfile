pipeline {
    agent any
    tools {
        maven 'localmvn'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                echo 'Building2..'
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
