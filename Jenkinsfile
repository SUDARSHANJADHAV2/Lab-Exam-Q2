
pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Fetching code from GitHub'

                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Python Docker Image'

                sh 'docker build -t python-square .'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Running Python Docker Container'

                sh 'docker run --rm python-square'
            }
        }

    }
}
