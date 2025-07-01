pipeline {
    agent any

    tools {
        maven 'maven3.9.6' // Le nom que tu as mis dans Jenkins
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ghofrane-dridi/devsecops-pipeline.git'
                echo "Code récupéré depuis Git"
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

