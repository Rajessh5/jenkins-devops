pipeline {
	agent any
	// agent { docker { image 'maven:3.8.6' } }
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build') {
			steps {
				sh 'maven --version'
				sh 'docker version'
				echo "Build"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID- $env.BUILD_ID"
				echo "Path - $env.PATH"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"
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
		changed {
			echo "I will execute when something chnage"
		}
	}
}