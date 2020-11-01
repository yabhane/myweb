pipeline{
	agent any
	
	environment {
		//PATH = "/opt/maven3/bin:$PATH"		
		//PATH = "/maven3/bin:$PATH"	
		PATH = "${PATH}:${getMavenPath()}"
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


def getMavenPath(){
	 def mvnHome = tool name: 'Maven3', type: 'maven'
	return "${mvnHome}/bin"
}
