pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application'
                sh 'test -f index.html'
            }
        }

        stage('Deploy') {
    steps {
        echo 'Deploying website to Nginx'
        sh 'cp index.html /var/www/html/index.html'
    }
}

    post {
        success {
            echo 'CI/CD pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD pipeline failed!'
        }
    }
}
