pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/DemoYourName.git'
            }
        }

        stage('Build') {
            steps {
                sh 'javac Lab3.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Lab3'
            }
        }
    }
}
