//Declartive scripting 
pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3' } } 
	environment {
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = '$dockerHome/bin:$mavenHome/bin:$PATH'
	}
		stages {
			stage ('Build') {
				steps {
					//sh 'mvn --version'
					echo "Build"
					echo "Path - $PATH"
					echo "BUILD_NUMBER - $env.BUILD_NUMBER"
					echo "BUILD_ID - $env.BUILD_ID"
					echo "JOB_NAME - $env.JOB_NAME"
					echo "BUILD_TAG - $env.BUILD_TAG"
					echo "BUILD_URL - $env.BUILD_URL "
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
