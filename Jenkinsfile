pipeline {
    agent any

    tools {
    maven 'Maven3'   // Must match exactly what Jenkins shows
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

