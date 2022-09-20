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
       stage('Deliver') { 
            steps {
                sh './jenkins/scripts/deliver.sh' 
<<<<<<< HEAD

		timeout(time: 1, unit: 'MINUTES') {
	                sh './jenkins/scripts/kill.sh' 
		}
=======
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './jenkins/scripts/kill.sh' 
>>>>>>> parent of 4b54747... Merubah mekanisme input message
            }
        }
    }
}
