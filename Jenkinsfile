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
				git 'https://github.com/yabhane/myweb'			
			   }
		}
		 stage('Compile-Package'){
			 steps{
	  	 //Get Maven home directory path
	 	 def mvnHome = tool name: 'Maven3', type: 'maven'
	   	//Using this path we are given path to mvn command
	  	 sh "${mvnHome}/bin/mvn package"
				 //Output : Created packages in war file
			 }
  		 }
	      	
		
		/*stage("Maven Build"){
			steps{
				sh "mvn clean package"			
			}
	      }*/
	}   
}


def getMavenPath(){
	 def mvnHome = tool name: 'Maven3', type: 'maven'
	return "${mvnHome}/bin"
}
