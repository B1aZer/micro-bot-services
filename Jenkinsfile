pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            script {
                echo 'go!'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'docker-compose up -d'
                }
            }
        }
    }
}