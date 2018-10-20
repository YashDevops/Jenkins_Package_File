pipeline {
	agent any
	stages{
	stage('package'){
	steps{

	steps {
                withMaven(maven : 'mvn') {
                    sh 'mvn clean compile'
                }
}
	
	
	}
	post{
	success{
	echo "Archiving Artifacts"
	archiveArtifacts artifacts: '**/target/*war'
	}
	}
	}
}
}