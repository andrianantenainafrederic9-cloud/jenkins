
pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Recuperation du projet React'
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

        stage('Verification') {
            steps {
                sh 'ls -la dist'
                echo 'Build React termine avec succes !'
            }
        }
    }

    post {
        success {
            echo 'Pipeline termine avec succes !'
        }

        failure {
            echo 'Une erreur est survenue.'
        }
    }
}
