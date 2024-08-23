pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building using Maven..."
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Testing using Selenium..."
            }
            post {
                success {
                    emailext(body: "Test was successful!", subject: "Test status email", to: "kanendc@gmail.com", attachLog: True)
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Code analysis using Synk Code..."
            }
        }
        stage('Security Scan') {
            steps {
                echo "Security scanning using SonarQube..."
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploying to AWS EC2 instance..."
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on the staging environment..."
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying to AWS EC2 instance..."
            }
        }
    }
}