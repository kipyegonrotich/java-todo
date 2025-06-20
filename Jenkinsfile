pipeline {
    agent any

    tools {
        gradle "Gradle-9"
    }

    stages {
        stage('Clone code') {
            steps {
                git branch: 'master', url: 'https://github.com/kipyegonrotich/java-todo.git'
            }
        }

        stage('Build code') {
            steps {
                sh './gradlew build'
            }
        }
        stage("Test code"){
            steps{
                sh './gradlew test'
            }
        }
    }
}