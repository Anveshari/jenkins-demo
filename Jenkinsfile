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
}
