pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/naine312/MyJavaProject.git',
                        credentialsId: 'fba0a49a-219b-4bc6-b13f-50515e8be95b'
                    ]]
                ])
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
