pipeline {
    agent { label 'maven-node' }

    tools {
        maven 'maven'
        jdk 'JDK'
        git 'git'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}