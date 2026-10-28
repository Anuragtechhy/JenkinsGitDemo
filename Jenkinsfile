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

        stage('Failure Demo') {
            steps {
                error 'Intentional failure to test post conditions'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check Console Output.'
        }

        always {
            echo 'Pipeline execution has finished.'
        }
    }
}
