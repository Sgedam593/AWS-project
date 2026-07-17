pipeline {

    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t santosh-devops:v2 .'
            }
        }

        stage('Tag Docker Image') {
            steps {
                sh 'docker tag santosh-devops:v2 sgedam123/santosh-devops:v2'
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USERNAME',
                    passwordVariable: 'DOCKER_PASSWORD'
                )]) {

                    sh '''
                    echo $DOCKER_PASSWORD | docker login -u $DOCKER_USERNAME --password-stdin
                    docker push sgedam123/santosh-devops:v2
                    '''
                }
            }
        }

    }
}
