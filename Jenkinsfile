def mvnHome
pipeline {
  environment {
    registry = "gilardoni72/docker-test"
    registryCredential =  'docker-hub-registry'
  }
	
	agent nodo
		stages{
			
			stage("GITHUB"){
				steps {
					 git branch: 'prueba', credentialsId: 'gittoken', url: 'https://github.com/gilardoni72/CI_CD_Integration.git'
				}
			}
		

			stage('Building image') {
				steps{
					script {
						docker.build registry + ":$BUILD_NUMBER"
					}
				}
			}

		


		}
	
}  
  
  
