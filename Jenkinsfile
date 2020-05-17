pipeline {
    agent { docker { image 'node:10' } }
    environment {
        HOME = '.'
        export GIT_COMMITTER_NAME='jeremypunsalan-dotcom'
        export GIT_COMMITTER_EMAIL='me@jeremypunsalan.com'
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