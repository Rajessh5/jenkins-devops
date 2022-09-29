pipeline {
	agent any
	stages{
		stage('Build') {
			step {
				echo "Build"
			}
		}
		stage('Test') {
			step {
				echo "Test"
			}
		}
		stage('Integration Test') {
			step {
				echo "Integration Test"
			}
		}
	}
	post {
		always {
			echo "I will run always"
		}
		success {
			echo "I will run when build success"
		}
		fail {
			echo "I  will run build fails"
		}
	}
}