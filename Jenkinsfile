pipeline
{
    agent any
    stages
    {
        stage('Maven Build')
        {
            steps
            {
                script
                {
                         git credentialsId: 'github-pwd', url: 'https://github.com/pkavyasree/simple-java-maven-app.git'
			 def mvnHome = tool name: 'maven', type: 'maven'
                         def mvnCMD = "/usr/local/src/apache-maven/bin/mvn"
                         sh "${mvnCMD} -f pom.xml clean package"
                }
            }
        }
    }  
                
                 
                 
