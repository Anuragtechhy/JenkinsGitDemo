pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                echo 'Checking Python installation'
                bat 'python --version'
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
