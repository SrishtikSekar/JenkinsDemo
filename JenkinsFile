pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/SrishtikSekar/JenkinsDemo.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*.*', fingerprint: true
            }
        }
    }
}