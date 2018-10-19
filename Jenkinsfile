pipeline {
	agent any
	tools {
    maven 'mvn'
  }
	stages{
	stage('package'){
	steps{
		sh 'mvn clean package'
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