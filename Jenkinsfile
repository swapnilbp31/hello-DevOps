pipeline {
    agent any
    stages {
        stage('Checkout'){
            steps {
                git branch: 'main' , url:'https://github.com/swapnilbp31/hello-DevOps.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Build stage started'
                sh 'python --version'
            }
        }
        stage('Run the application'){
            steps{
                sh 'python aap.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Ran Successfully'
        }
    failure {
        echo 'Pipeline Failed'
    }
    }
}