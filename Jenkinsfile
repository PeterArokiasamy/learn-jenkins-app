	pipeline {
	    agent any
	
	    stages {
	        stage('Build') {
	            agent {
	                docker {
	                    image 'node:18-alpine'
	                    reuseNode true
	                }
	            }
	            steps {
	                sh '''
	                    ls -la
	                    node --version
	                    npm --version
		                #Instead of Install use CI based commands
	                    npm ci
	                    npm run build
	                    ls -la
	                '''
	            }
	        }
	    }
}