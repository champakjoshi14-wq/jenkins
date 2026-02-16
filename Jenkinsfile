pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/champakjoshi14-wq/jenkins.git'
            }
        }

        stage('Run Python Script') {
            steps {
                sh 'python3 main.py'
            }
        }
    }

    post {
        success {
            echo 'Python script ran successfully!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
