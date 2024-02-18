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
        
        stage('Testing') {
            steps {
                echo "Testing"
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