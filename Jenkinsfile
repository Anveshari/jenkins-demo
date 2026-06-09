pipeline {
    agent any
    parameters {
        string(
            name: 'ENVIROMENT',
            defaultvalue: 'dev',
            description: 'Deployment enviroment'
        )

    stages {
        stage('Test') {
            steps {
                echo "Enviroment: ${params.ENVIROMENT}"
            }
        }

        stage('Checkout') {
            steps {
                checkout scm
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

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }
    }
}
