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
                sh 'export NPM_CONFIG_GLOBALCONFIG="$(pwd)/npmrc" && npm config set cache $(pwd)/.npm-cache && npm install' 
            }
        }
    }
}