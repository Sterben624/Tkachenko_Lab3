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
                bat 'mvn tomcat:redeploy'
            }
        }
        stage('Run JMeter Test') {
            steps {
                // Крок для виконання тестування продуктивності в JMeter
                bat '"C:\Program Files\apache-jmeter-5.6\bin\jmeter" -n -t "F:\TestLab4Tkachenko.jmx" -l "F:\Learning\EngineeringSoft\result.jtl"'
            }
        }
}
