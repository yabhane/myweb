pipeline{
	agent any
	
	environment {
		PATH = "/opt/maven3/bin:$PATH"
		
	}
	stages{
	
		stage("SCM - Checkout"){
			steps{
				git CredentialsId 'github', url: 'https://github.com/yabhane/myweb'
			
			}
		}
		
	      stage("Maven Build"){
			steps{
				sh "mvn clen package"			
			}
	      }
	   
}


