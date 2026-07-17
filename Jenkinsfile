pipeline {

    agent any

    stages {

        stage('GitHub Connected') {
            steps {
                echo 'GitHub Connected Successfully'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t santosh-devops:v2 .'
            }
        }

    }
}
