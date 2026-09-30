pipeline {
    agent any

    stages {

        stage('Install Backend') {
            steps {
                dir('backend') {
                    bat 'npm install'
                }
            }
        }

        stage('Install Frontend') {
            steps {
                dir('frontend') {
                    bat 'npm install'
                }
            }
        }

        stage('Test Backend') {
            steps {
                dir('backend') {
                    bat 'npm test'
                }
            }
        }

        stage('Lint Frontend') {
            steps {
                dir('frontend') {
                    bat 'npm run lint'
                }
            }
        }

        stage('Build Frontend') {
            steps {
                dir('frontend') {
                    bat 'npm run build'
                }
            }
        }
    }
}