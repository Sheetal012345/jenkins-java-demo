pipeline {
    agent any

    stages {

        stage('Fetch File') {
            steps {
                git branch: 'main', url: 'https://github.com/Sheetal012345/jenkins-java-demo.git'
            }
        }

        stage('Building') {
            steps {
                echo 'Building Project....'
                bat 'javac Hello.java'
            }
        }

        stage('Execution') {
            steps {
                echo 'Executing Program'
                bat 'java Hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Executed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}
