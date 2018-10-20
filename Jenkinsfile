pipeline{
		agent any
			stages{
				stage('build'){
					steps{
						git url:'https://github.com/YashDevops/MMTPOC.git'
						withMaven(maven:'mvn'){
							sh 'mvn clean install'
						}
					}
				}
				stage('test'){
					steps{
						git url:'https://github.com/YashDevops/MMTPOC.git'
						withMaven(maven:'mvn'){
							sh 'mvn test -Dskiptests'
						}
					}
					post{
						always{
							echo "Hi this is to make that test step has been completed"
						}
					 	success{
					 		echo "Though build has been passed but test cases has been skipped"
					 	}
					}
				}
				stage('Package'){
					steps{
						git url:'https://github.com/YashDevops/MMTPOC.git'
						withMaven(maven:'mvn'){
							sh 'mvn package'
						}
					}
				}

			}
}