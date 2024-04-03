pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Крок для клонування репозиторію з GitHub
                git 'https://github.com/Sterben624/Tkachenko_Lab3.git'
            }
        }
        stage('Build and Deploy') {
            steps {
                // Крок для перевиклику цілей Maven верхнього рівня для перевищення tomcat7:redeploy
                bat 'mvn package'
            }
        }
    }
}
