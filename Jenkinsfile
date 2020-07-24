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
    }
}
