
pipeline{
	agent any
	stages{
		stage('build'){
			steps{
				git url:'https://github.com/YashDevops/MMTPOC.git'
			}
			steps{
			 withMaven(maven : 'mvn') {
                    sh 'mvn clean compile'}
			}
		}
	}
}
