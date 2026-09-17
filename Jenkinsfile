pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'javac calculator.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java calculator'
            }
        }
    }

    post {
        success {
            echo 'Calculator executed successfully!'
        }

        failure {
            echo 'Calculator build failed!'
        }
    }
}