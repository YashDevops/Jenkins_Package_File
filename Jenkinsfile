pipeline{
		agent any
			stages{
				stage('build'){
					steps{
						git url:'https://github.com/YashDevops/MMTPOC.git'
						withMaven(maven:'mvn'){
							sh 'mvn clean compile'
						}
					}
					post{
						always{
							echo "This is to confirm that install has been success"
						}
						success{
							echo "This is to make sure that the build has been success"
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