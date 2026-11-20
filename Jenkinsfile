pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Java application'
                bat 'javac Main.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Java application'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java Main'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline successful'
        }
        failure {
            echo 'CI pipeline failed'
        }
    }
}
