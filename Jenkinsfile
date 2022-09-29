pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
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
		failure {
			echo "I  will run build fails"
		}
	}
}