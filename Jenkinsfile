pipeline {
    agent { docker { image 'node:8.12.0' } }
    environment {
        HOME = '.'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
                sh 'rm -rf node_modules/gh-pages/.cache'  
            }
        }
        stage('Deploy to GitHub Pages') { 
            steps {
                sh 'npm run build' 
                sh 'npm run deploy'
            }
        }
   	
    }
}