pipeline
{
    agent any
    stages
    {
        stage('Cloning repo')
        {
            steps
            {
                script
                {
                         git credentialsId: 'github-pwd', url: 'https://github.com/pkavyasree/simple-java-maven-app.git'
			
                }
            }
        }
	stage('Maven Build')   
	    {
             steps
	 {
	 script
		 {
		 def mvnHome = tool name: 'maven', type: 'maven'
                 def mvnCMD = "/usr/share/maven/bin/mvn"
                 sh "${mvnCMD} -f pom.xml clean package"
	    
    }  
}             
                 
	    }
    }
}
