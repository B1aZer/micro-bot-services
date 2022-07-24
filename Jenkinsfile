pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
            }
            steps {
                script {
                    sh 'ls -la'
                }
            }
            steps {
                sh '''
                    docker verion
                    docker-compose version
                '''
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