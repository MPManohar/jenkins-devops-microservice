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
				echo 'Hi "run always message " if it is successful or not  '
			}
			success {
				echo 'Sucessfull message, Runs after the build is sucess'
			}
			failure {
				echo 'UnSuccessfull message, prints if there is any failure on the build '
		}
	}	
}
