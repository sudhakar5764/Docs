pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/python']], extensions: [], userRemoteConfigs: [[credentialsId: 'f4bfe740-aa50-4e54-8b4e-044c111931d3', url: 'https://github.com/sudhakar5764/Docs.git']])
            }
        }
        stage('Git Build') {
            steps {
                 git branch: 'python', credentialsId: 'f4bfe740-aa50-4e54-8b4e-044c111931d3', url: 'https://github.com/sudhakar5764/Docs.git'
            }
        }
        stage('Testing') {
            steps {
                echo 'print "Test is completed"'
            }
        }
        
    }
}
