pipeline{
    agent any

    tools{
        jdk 'jdk8'
        maven 'maven3'
    }

    stages{
        stage('Test'){
            steps{
                script{
                    bat 'mvn clean test'
                }
            }
        }
        stage('reports') {
            steps {
                script {
                    allure([
                            includeProperties: false,
                            jdk: '1.8',
                            properties: [],
                            reportBuildPolicy: 'ALWAYS',
                            results: [[path: 'target/allure-results']]
                    ])
                }
            }
        }
    }
}
