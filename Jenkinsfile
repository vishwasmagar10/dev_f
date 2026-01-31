pipeline {
	agent any
	environment {
		DOCKERHUB_CRED=credentials('dockerhub1')
		IMAGE_NAME="vishwasmagar10/dev_f"
	}

	 // triggers {
  //       cron('* * * * *')
  //   }
	
	stages {
		stage('checkout') {
			steps {
				git url:'https://github.com/vishwasmagar10/dev_f/', branch:'main' 
			}
		}
		
		stage('Build Docker Image') {
			steps {
				script {
					dockerImage=docker.build("${IMAGE_NAME}:latest")
				}
			}
		}
		
		stage('Push to DockerHub') {
			steps {
				script {
					docker.withRegistry('https://index.docker.io/v1/','dockerhub1') {
						dockerImage.push()
					}
				}
			}
		}
	}
	
	
}
