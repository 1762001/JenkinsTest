pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
        y
                script {
                    git 'https://github.com/1762001/JenkinsTest.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                
                sh 'mvn clean install'
            }
        }
        
        stage('Deploy') {
            steps {
                
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
