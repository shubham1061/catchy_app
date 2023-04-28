pipeline {

    agent any

    stages {

        stage("Git Checkout"){
            steps {
                git branch: 'main', url: 'https://github.com/Shubhamvarora/catchy_app.git'
            }
        }

        stage("Unit Testing"){
            steps {
                sh 'mvn test'
            }
        }

        stage("Integration Testing"){
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }

        stage("Build"){
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
