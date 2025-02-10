pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/NavinSubramanian/jenkinsdt3.git'
            }
        }
        stage('Build') {
            steps {
                bat 'make'
                bat 'hello.exe'
            }
        }
    }
}
