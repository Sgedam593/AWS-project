pipeline {

    agent any

    stages {

        stage('GitHub Connected') {
            steps {
                echo 'GitHub Connection Successful'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t santosh-devops:v2 .'
            }
        }

    }
}
