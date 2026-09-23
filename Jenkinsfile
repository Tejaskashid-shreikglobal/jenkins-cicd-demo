pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mkdir -p build && cp index.html build/'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f build/index.html'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deployment successful'
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
