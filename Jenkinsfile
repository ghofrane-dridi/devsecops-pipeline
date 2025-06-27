pipeline {
    agent any
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

