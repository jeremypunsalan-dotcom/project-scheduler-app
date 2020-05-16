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
                sh 'npm install'
                sh 'rm -rf node_modules/gh-pages/.cache'  
            }
        }
        stage('Deploy to GitHub Pages') { 
            steps {
                sh 'npm run build' 
            }
        }
   	
    }
}