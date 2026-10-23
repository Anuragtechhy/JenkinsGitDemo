pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                echo 'Checking Python installation'
                bat 'python --version'
            }
        }

        stage('Pipeline Update Check') {
            steps {
                echo 'Updated Jenkinsfile loaded from GitHub!'
            }
        }

        stage('Run Program') {
            steps {
                echo 'Running Python program'
                bat 'python main.py'
            }
        }
    }
}
