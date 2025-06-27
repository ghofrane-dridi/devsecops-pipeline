pipeline {
    agent any
    tools {
        jdk 'Java 17'
        maven 'Maven 3.9.6'
    }
    stages {
        stage('Clone') {
            steps {
                git branch: 'dridi_ghofrane', url: 'https://github.com/ghofrane-dridi/devsecops-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}

