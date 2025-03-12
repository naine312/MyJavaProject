pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    credentialsId: 'fba0a49a-219b-4bc6-b13f-50515e8be95b', 
                    url: 'https://github.com/naine312/MyJavaProject.git'
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
