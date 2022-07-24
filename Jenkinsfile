pipeline {
    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'ls -la'
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