pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
       stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
       stage('Deploy') { 
            steps {
		timeout(time: 1, unit: 'MINUTES') {

	                sh './jenkins/scripts/deliver.sh' 
		}

                sh './jenkins/scripts/kill.sh' 
            }
        }
    }
}
