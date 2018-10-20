
pipeline{
	agent any
	stages{

		stage('Clone repo'){
			GIT_URL:'https://github.com/YashDevops/MMTPOC.git'
		}
		stage('build'){
			steps{
			 withMaven(maven : 'mvn') {
                    sh 'mvn clean compile'}
			}
		}
	}
}
