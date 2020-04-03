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
			stage ('Checkout') {
				steps {
					sh 'mvn --version'
					sh 'docker version'
					echo "Build"
					echo "Path - $PATH"
					echo "BUILD_NUMBER - $env.BUILD_NUMBER"
					echo "BUILD_ID - $env.BUILD_ID"
					echo "JOB_NAME - $env.JOB_NAME"
					echo "BUILD_TAG - $env.BUILD_TAG"
					echo "BUILD_URL - $env.BUILD_URL "
			}
		}
			stage ('Compile') {
				steps{
					sh "mvn clean compile"
				}
			}
			stage ('Test') {
				steps { 
					echo "Test"
					sh "mvn test"
			}
		}
			stage ('Intergration Test') {
				steps {
					echo "IntegrationTest"
					sh "mvn failsafe:integration-test failsafe:verfiy"
			}
		}
	}	

}
