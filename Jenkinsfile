pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/shreyas-poojar/CI_WEB_APP.git
            }
        }

        stage('Verify Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t myapp:latest .'
            }
        }

        stage('Docker Run') {
            steps {
                bat 'docker run -d -p 8080:80 myapp:latest'
            }
        }
    }
}