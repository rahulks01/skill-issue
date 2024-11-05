pipeline {
    agent any  // Use any available agent or executor (this allows the pipeline to run on any available node in Jenkins).

    environment {
        DEPLOY_ENV = 'staging'  // Define the environment variable for deployment (can be accessed as ${DEPLOY_ENV} in later stages).
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git 'https://github.com/rahulks01/skill-issue.git'  // This clones the Git repository.
            }
        }

        stage('Build') {
            steps {
                // Print a message or run actual build commands here
                sh 'echo "Building application..."'  // This is a placeholder. Replace with actual build commands (e.g., `mvn clean install` for Maven).
            }
        }

        stage('Test') {
            steps {
                // Print a message or run testing commands here
                sh 'echo "Running tests..."'  // This is a placeholder. Replace with testing commands (e.g., `mvn test` for Maven).
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application
                sh 'echo "Deploying to ${DEPLOY_ENV} environment..."'  // This prints a message indicating deployment to the staging environment.
                // Replace this with actual deployment commands, like `scp` for file transfer or remote deployment commands.
            }
        }
    }

    post {
        always {
            // Clean up workspace after the pipeline completes
            echo 'Cleaning up...'
            deleteDir()  // This will delete the workspace after the pipeline has run.
        }
    }
}
