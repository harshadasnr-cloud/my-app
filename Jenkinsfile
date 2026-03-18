pipeline {
    agent { label 'maven-node' }   // IMPORTANT (your slave label)

    tools {
        maven 'maven'
        jdk 'JDK'
        git 'git'   // 👈 ADD THIS LINE
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-repo.git'
            }
        }

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