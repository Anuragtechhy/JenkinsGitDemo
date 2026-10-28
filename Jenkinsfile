pipeline {
    agent any

    environment {
    APP_NAME = 'HRMS'
    TEST_ENV = 'QA'
}

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

        stage('Show Environment') {
    steps {
        echo "Application: ${env.APP_NAME}"
        echo "Test environment: ${env.TEST_ENV}"
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
