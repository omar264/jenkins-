pipeline {
    agent any
    tools{ jdk 'jdk17' }
    environment { JAVA_HOME = 'C:\\Program Files\\Java\\jdk-17' }
    stages {
        stage ('Compile Stage') {
            steps {
                withMaven(maven : 'maven3.8.6') {
                    bat 'mvn clean compile'
                }
            }
        }
        stage ('Testing Stage') {
            steps {
                withMaven(maven : 'maven3.8.6') {
                    bat 'mvn test'
                }
            }
        }
        stage ('Install Stage') {
            steps {
                withMaven(maven : 'maven3.8.6') {
                    bat 'mvn install -Dmaven.test.skip=true'
                } 
            } 
        } 
    }
}
