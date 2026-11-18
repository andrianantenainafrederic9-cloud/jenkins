
pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {
        stage('Verification') {
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('Installation') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build React') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Verification du build') {
            steps {
                sh 'ls -la dist'
            }
        }
    }

    post {
        success {
            echo 'Build React reussi !'
        }

        failure {
            echo 'Une erreur est survenue.'
        }
    }
}
