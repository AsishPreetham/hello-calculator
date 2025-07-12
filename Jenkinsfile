pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AsishPreetham/hello-calculator.git'
            }
    }


        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test Results') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }
        }
    }
}

