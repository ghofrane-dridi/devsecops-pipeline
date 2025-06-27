pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'dridi_ghofrane', url: 'https://github.com/ghofrane-dridi/devsecops-pipeline.git'
            }
        }
        stage('Check Java and Maven version') {
            steps {
                sh 'java -version'
                sh 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests=true'
            }
        }
    }
}

