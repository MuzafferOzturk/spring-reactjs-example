pipeline {
    agent any
    stages {
            stage('Compile Stage') {
                steps {
                    withMaven(maven: '3-6-3'){
                        sh 'mvn clean compile'
                    }
                }
            }
            stage('Test') {
                steps {
                    withMaven(maven: '3-6-3'){
                        sh 'mvn test'
                    }
                }
            }
            stage('Deployment') {
                steps {
                    withMaven(maven: '3-6-3'){
                        sh 'mvn deploy'
                    }
                }
            }
        }
}