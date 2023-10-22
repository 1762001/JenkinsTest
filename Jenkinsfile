pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // This stage checks out the code from the Git repository
                script {
                    git 'https://github.com/your-username/your-repo.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                // This stage builds the Java project (replace 'mvn clean install' with your build command)
                sh 'mvn clean install'
            }
        }
        
        stage('Deploy') {
            steps {
                // This stage deploys the application (replace 'echo' with your deployment command)
                echo 'Deployment completed successfully!'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully! Deploy your application to production.'
        }
        failure {
            echo 'Pipeline failed. Please check the build and deployment logs for errors.'
        }
    }
}
