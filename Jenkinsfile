pipeline {
    agent any
    tools {
        maven 'maven'
    }
    environment {
        DOCKER_IMAGE = 'Myimage'
    }
    stages {
        stage('Clean Workspace') {
            steps{
                cleanWs()
            }
        }

        stage('Build') {
            steps {
              sh 'pwd'
              sh 'mvn package'
            }
        }
        stage('Docker Image') {
            steps {
                sh 'echo ${DOCKER_IMAGE} '
            }
        }
    }
}
