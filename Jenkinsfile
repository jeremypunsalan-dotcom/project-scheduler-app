pipeline {
    agent any
    stages {
        stage('Install) { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Clear cache') { 
            steps {
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