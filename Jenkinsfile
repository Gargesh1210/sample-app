pipeline {
    agent any
    tools {
        maven 'Maven3'   // the name you gave Maven in Global Tool Config
        jdk 'JDK11'      // the name you gave JDK in Global Tool Config
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Gargesh1210/sample-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Run') {
            steps {
                sh 'java -jar target/sample-app-1.0-SNAPSHOT.jar'
            }
        }
    }
}

