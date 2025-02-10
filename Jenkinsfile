pipeline {
    agent any
    environment {
        PATH = "C:\\WINDOWS\\SYSTEM32"
        CPPPATH = 'C:\\msys64\\mingw64\\bin'
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
                set PATH=%CPPPATH%;%PATH%
                g++ -o hello main.cpp
                hello.exe
                '''
            }
        }
    }
}
