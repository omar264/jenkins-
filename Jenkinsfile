pipeline {
    agent any
    tools{ jdk 'JDK17' }
    environment { JAVA_HOME = 'C:\\Program Files\\Java\\jdk-17' }
    stages {
        stage ('Compile Stage') {
            steps {
                withMaven(maven : 'maven3.9.8') {
                    bat 'mvn clean compile'
                }
            }
        }
        stage ('Testing Stage') {
            steps {
                withMaven(maven : 'maven3.9.8') {
                    bat 'mvn test'
                } 
            }
        }
        stage ('Install Stage') {
            steps {
                withMaven(maven : 'maven3.9.8') {
                    bat 'mvn install'
                } 
            } 
        } 
    }
}
