pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            steps {
                echo 'go..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}