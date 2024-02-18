pipeline {
    agent {
        node {
            label 'devops1-jundi'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo "Build"
                sh '''
                cd apps
                npm install
                '''
            }
        }

        stage('Copy Env') {
            steps {
                echo "Copy env"
                sh '''
                copy /root/simple-apps/.env apps/
                '''
            }
        }
        
        stage('Testing') {
            steps {
                echo "Testing"
                sh '''
                cd apps
                npm test
                npm run test:coverage
                '''
            }
        }

        stage('Scanning') {
            steps {
                echo "Scanning"
            }
        }
        stage('Containerized') {
            steps {
                echo "Containerized"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }
        stage('Publish') {
            steps {
                echo "Publish"
            }
        }

    }
}