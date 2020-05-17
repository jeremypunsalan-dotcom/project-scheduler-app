pipeline {
    agent { docker { image 'node:8.12.0' } }
    environment {
        HOME = '.'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Deploy to GitHub Pages') { 
            steps {
                sh 'rm -rf node_modules/gh-pages/.cache'
                sh 'npm run deploy'
            }
        }
   	
    }
}