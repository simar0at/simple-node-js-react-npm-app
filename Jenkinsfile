pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm --globalconfig $(pwd)/npmrc config set cache $(pwd)/.npm-cache && npm --globalconfig $(pwd)/npmrc install' 
            }
        }
    }
}