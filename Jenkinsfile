pipeline {
    agent { label 'maven-node' }   // IMPORTANT (your slave label)

    tools {
        maven 'maven'
        jdk 'JDK'
        git 'git'   // 👈 ADD THIS LINE
    }

    stages {
         stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }
         stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Clone') {
            steps {
              
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