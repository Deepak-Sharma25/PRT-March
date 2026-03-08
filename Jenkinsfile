pipeline {
    agent any

    stages {

        stage('Pull Source Code') {
            steps {
                git branch: 'main', url: 'https://github.com/your-username/project-repo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("prt-app:latest")
                }
            }
        }

    }

    post {
        success {
            echo "Docker image built successfully!"
        }

        failure {
            echo "Pipeline failed."
        }
    }
}
