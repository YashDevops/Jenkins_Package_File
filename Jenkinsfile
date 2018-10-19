pipeline {
	agent any
	 tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
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