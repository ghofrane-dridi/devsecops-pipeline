pipeline {
    agent any

    environment {
        JAVA_TOOL_OPTIONS = '--add-opens java.base/java.lang=ALL-UNNAMED'
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'dridi_ghofrane', url: 'https://github.com/ghofrane-dridi/devsecops-pipeline.git'
                echo "Code récupéré depuis Git"
            }
        }

        stage('Check Java and Maven version') {
            steps {
                sh 'java -version'
                sh 'mvn -v'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}

