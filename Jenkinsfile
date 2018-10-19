pipeline {
	agent any
	 tools { 
        maven 'Maven 3.5.4' 
        
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