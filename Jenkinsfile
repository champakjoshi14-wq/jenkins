pipeline {
    // 'agent any' means this pipeline can run on any available Jenkins node/agent
    agent any

    stages {

        stage('Checkout') {
            steps {
                // This step clones the source code from your GitHub repository

                // 'branch: main' tells Jenkins to pull code from the MAIN branch
                // 'url' is the GitHub repository location
                git branch: 'main',
                    url: 'https://github.com/champakjoshi14-wq/jenkins.git'
            }
        }

        stage('Run Python Script') {
            steps {
                // Since your Jenkins is running on WINDOWS,
                // we use 'bat' instead of 'sh' (which is for Linux)

                // This command runs your Python file: main.py
                bat 'python main.py'
            }
        }
    }

    post {

        // This block runs ONLY if the pipeline is successful
        success {
            // Prints a success message in Jenkins console output
            echo 'Python script ran successfully!'
        }

        // This block runs if ANY stage in the pipeline fails
        failure {
            // Prints a failure message in Jenkins console output
            echo 'Build failed.'
        }
    }
}
