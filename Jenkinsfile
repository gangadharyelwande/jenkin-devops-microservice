/*node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Integration Test"
	}
}*/

//declarative

pipeline{
	//agent any

	agent { docker 
		{ 
			image 'maven: 3.6.3' 
			args '-u root:root'
		} 
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	} 
	
	post {
		always{
			echo 'I am awesome, I run always'
		}
		success{
			echo 'I will run when you are successful'
		}
		failure{
			echo 'I will run when you are fail'
		}
	}
}
