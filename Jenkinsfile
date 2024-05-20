pipeline {
    agent any

    stages {
        stage('build-docker-image') {
            steps{
                obtain_code_poll_true()
                build_and_push_docker_image()
            }
        }
    }
}


def obtain_code_poll_true() {
    git branch: 'main', url: 'https://github.com/StepansSotskovsTestdevlabCom/course-js-api-framework.git'
}

def build_and_push_docker_image() {
    sh 'docker build --no-cache -t stepanssotskovs/api-tests:latest .'
    sh 'docker push stepanssotskovs/api-tests:latest'
}