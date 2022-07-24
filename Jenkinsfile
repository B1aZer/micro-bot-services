pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'ls -la'
                sh '''
                    pwd
                    cd /home/terraform
                    pwd
                    whoami
                    ssh terraform@3.80.214.242 -i tf-packer ./dockerRun.sh
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