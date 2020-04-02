//Declartive scripting 
pipeline {
	agent any 
		stages {
			stage ('Build') {
				steps {
					echo " Build"
			}
		}
			stage ('Test') {
				steps { 
					echo "Test"
			}
		}
			stage ('Intergration Test') {
				steps {
					echo "IntegrationTest"
			}
		}
	}	
	post { 
			always {
				echo 'run always message '
			}
			success {
				echo 'Sucessfull message'
			}
			failure {
				echo 'UnSuccessfull message'
		}
	}	
}
