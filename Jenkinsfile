pipeline {
    agent any

    stages {
        stage('build-docker-image') {
            steps{
                build_docker_image()
            }
        }
    }
}


def build_docker_image() {
    echo "Build api-tests.. "
    sh 'docker build --no-cache -t stepanssotskovs/api-tests:latest .'
    sh 'docker push stepanssotskovs/api-tests:latest'
}