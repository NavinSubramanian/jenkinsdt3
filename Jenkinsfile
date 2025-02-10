pipeline {
    agent any
    environment {
        PATH = "C:\\WINDOWS\\SYSTEM32"
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/NavinSubramanian/jenkinsdt3.git'
            }
        }
        stage('Build'){
            steps{
                bat '''
                set PATH=%PATH%
                make
                hello.exe
                '''
            }
        }
    }
}
