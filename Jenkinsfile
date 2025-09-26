pipeline {
    agent {
        label 'worker'
    }
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
        stage('CheckOut') {
            steps{
                git url: 'https://github.com/vineethkumar3/Sample-Java.git', branch: params.Branch
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
