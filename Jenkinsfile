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

	/*agent { docker 
		{ 
			image 'maven: 3.6.3' 
			//args '-u root:root'
			//args '--tmpfs /.config'
		} 
	}*/
	stages{
		stage('Build'){
			steps{
				//sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
