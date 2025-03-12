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

        stage('Check Files') {
            steps {
                sh 'ls -R'
            }
        }

        stage('Build') {
            steps {
                // Ensure the 'out' directory exists and compile the java files
                sh 'mkdir -p out'
                sh 'javac -d out src/main/java/com/sheridan/Main.java'
            }
        }

        stage('Run') {
            steps {
                // Run the compiled Java program
                sh 'java -cp out com.sheridan.Main'
            }
        }
    }
}
