pipeline {
    agent any

    tools {
        maven 'maven3'
        jdk 'jdk21'
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Verify Build') {
            steps {
                sh 'ls -l target'
            }
        }
    }
}