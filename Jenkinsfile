pipeline{
	agent any
	
	environment {
		PATH = "/opt/maven3/bin:$PATH"		
	}
	stages{	
		stage("SCM - Checkout"){
			steps{
				//git CredentialsId 'github', url: 'https://github.com/yabhane/myweb'			
				git 'https://github.com/yabhane/myweb'			
			   }
		}
		
	      stage("Maven Build"){
			steps{
				sh "mvn clean package"			
			}
	      }
	}   
}


