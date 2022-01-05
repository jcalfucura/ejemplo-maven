
pipeline {
    agent any
    stages {
        stage("step 1: Compile"){
            steps {
                script {
                sh "echo 'Compile'"
                sh "mvn clean compile -e"
                }
            }
        }
        stage("step 2: Test"){
            steps {
                script {
                sh "echo 'Test'"
                sh "mvn clean test -e"
                }
            }
        }
        stage("step 3: package .Jar"){
            steps {
                script {
                sh "echo 'Build'"
                sh "mvn clean package -e"
                }
            }
        stage("step 4: run"){
            steps {
                script {
                sh "echo 'run'"
                sh "maven mvn spring-boot:run"
                }
            }
        }
    }
}