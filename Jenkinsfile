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
       stage('Deliver') { 
            steps {
<<<<<<< HEAD
                sh './jenkins/scripts/deliver.sh' 
<<<<<<< HEAD

=======
>>>>>>> parent of f109559... Mengubah mekanisme input message
		timeout(time: 1, unit: 'MINUTES') {

	                sh './jenkins/scripts/deliver.sh' 
		}
<<<<<<< HEAD
=======
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './jenkins/scripts/kill.sh' 
>>>>>>> parent of 4b54747... Merubah mekanisme input message
=======

                sh './jenkins/scripts/kill.sh' 
>>>>>>> parent of f109559... Mengubah mekanisme input message
            }
        }
=======
>>>>>>> parent of e877db7... Add Deliver stage
    }
}
