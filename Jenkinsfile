pipeline {
    agent any
        stages {
            stage('Checkout') {
                steps {
                    git 'https://github.com/SUDARSHANJADHAV2/Lab-Exam-Q2.git'
                }
            }
            stage('Build') {
                steps {
                    sh 'docker build -t python-app .'
                }
            }
            stage('Run') {
                steps {
                    sh 'docker run -it --rm python-app'
                }
            }
        }
}

