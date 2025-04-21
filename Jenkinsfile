pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the repo...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t jenkins-hello .'
            }
        }
        stage('Run') {
            steps {
                echo 'Running hello.sh'
                sh 'chmod +x hello.sh && ./hello.sh'
            }
        }
    }
}
