pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('aaniketttt/lab7')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Stop and remove the container if it already exists
                    sh 'docker stop my_container || true'
                    sh 'docker rm my_container || true'

                    // Run the container in daemon mode (-d)
                    sh 'docker run -d --name my_container aaniketttt/lab7'
                }
            }
        }
    }
}
