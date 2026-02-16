pipeline {
    agent any

    environment {
        // If you need to set up any environment variables (e.g., Python version), you can define them here
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your Git repository
                git 'https://github.com/champakjoshi14-wq/jenkins/jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Python dependencies if you have a requirements.txt (optional)
                // Uncomment the following line if you have a 'requirements.txt' file
                // sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Python Script') {
            steps {
                // Run your Python script (main.py)
                sh 'python main.py'
            }
        }
    }

    post {
        always {
            // Actions to run after the pipeline finishes, like cleanup or notifications
            echo 'Cleaning up...'
        }

        success {
            // Actions for successful builds
            echo 'Build and script execution succeeded!'
        }

        failure {
            // Actions for failed builds
            echo 'Build or script execution failed.'
        }
    }
}
