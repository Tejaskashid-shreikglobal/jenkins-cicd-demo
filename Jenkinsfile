pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mkdir -p build'
                sh 'cp index.html build/index.html'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f build/index.html'
            }
        }

        stage('Deploy') {
            steps {
                sh 'cp build/index.html /var/www/html/index.html'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }
        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}
