pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ChakraHs/Basic-Spring.git', branch: 'main'
            }
        }

        stage('Display Message') {
            steps {
                // Display a message indicating successful Git checkout
                echo 'Git checkout successful! Repository cloned.'
            }
        }

        stage('Build') {
            steps {
                withEnv(["PATH+MAVEN=C:\\Program Files\\apache-maven-3.9.9"]) {
                    bat 'mvn clean install'
                }
            }
        }

        stage('mvn clean package successful passed') {
            steps {
                echo 'mvn clean install successful!'
            }
        }
    }
}
