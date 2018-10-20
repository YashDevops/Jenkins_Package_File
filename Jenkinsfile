
pipeline{
	agent any
	stages{

		stage('Clone repo'){
			git url:'https://github.com/YashDevops/MMTPOC.git'
		}
		stage('build'){
			steps{
			 withMaven(maven : 'mvn') {
                    sh 'mvn clean compile'}
			}
		}
	}
}
