pipeline {
	agent { docker 'gradle:4.5-jdk8-alpine' }
	stages {
		stage ( 'checkout' ){
			steps{
				sh 'gradle clean build'
				junit 'build/test-results/test/TEST-*.xml'
			}
		}
		stage ('deploy-stage' ){
			steps{
				echo "Deploying to stage"
			}
		}
		stage ( 'deploy-production' ){
			steps{
				echo "Deploying to production"
			}
		}
	}
}