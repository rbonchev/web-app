pipeline {
    agent any

    stages {
        stage("Build docker image") {
            steps {
                sh 'docker build -t web-app-image .'
            }
        }

        stage("Push docker image to Dockerhub") {
            steps {
                sh 'docker login -u rbonchev -p Shlqdkievraci44!'
                sh 'docker tag my-app-image rbonchev/web-app-image:latest'
                sh 'docker push rbonchev/web-app-image:latest'
            }
        }
    }
}