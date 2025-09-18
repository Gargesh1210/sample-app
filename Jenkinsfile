pipeline {
    agent any

    tools {
        maven 'maven3'   // Make sure this matches Jenkins Global Tool Config
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Run') {
            steps {
                sh 'mvn spring-boot:run'
            }
        }
    }
}

