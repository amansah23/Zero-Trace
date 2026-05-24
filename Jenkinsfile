pipeline {
    agent any

    environment {
        MONGO_URI = credentials('mongo_uri')
        JWT_SECRET = credentials('jwt_secret')
        ENCRYPTION_KEY = credentials('encryption_key')
        ADMIN_PASSWORD = credentials('admin_password')
    }

    stages {

        stage('Create Environment File') {
            steps {
                sh '''
                echo "PORT=5000" > backend/.env
                echo "MONGO_URI=$MONGO_URI" >> backend/.env
                echo "JWT_SECRET=$JWT_SECRET" >> backend/.env
                echo "ENCRYPTION_KEY=$ENCRYPTION_KEY" >> backend/.env
                echo "ADMIN_PASSWORD=$ADMIN_PASSWORD" >> backend/.env
                '''
            }
        }

        stage('Stop Old Containers') {
            steps {
                sh 'docker-compose down || true'
            }
        }

        stage('Build Containers') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Start Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }

    }
}