//Declartive scripting 
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3' } } 
		stages {
			stage ('Build') {
				steps {
					sh 'maven --version'
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
	
}
