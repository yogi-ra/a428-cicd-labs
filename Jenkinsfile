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
<<<<<<< HEAD
       stage('Deploy') { 
            steps {
		timeout(time: 1, unit: 'MINUTES') {

	                sh './jenkins/scripts/deliver.sh' 
#                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
		}

                sh './jenkins/scripts/kill.sh' 
            }
        }
=======
>>>>>>> parent of e877db7... Add Deliver stage
    }
}
