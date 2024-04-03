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
        stage('Run JMeter Test') {
            steps {
                // Крок для виконання тестування продуктивності в JMeter
                bat '"C:\\Program Files\\apache-jmeter-5.6.3\\bin\\jmeter" -n -t "F:\\TestPlan.jmx" -l "F:\\result.jtl"'
            }
        }
    }
}
