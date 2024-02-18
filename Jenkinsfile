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
                cp /root/simple-apps/apps/.env apps/
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
                sh '''
                cd apps
                sonar-scanner   -Dsonar.projectKey=Simple-Apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.10.11:9000   -Dsonar.login=sqp_e3243d58d04a5e3f3c5f9de6340372fdeb182db9
                '''
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