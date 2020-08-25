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
                         git credentialsId: 'c810e053-5812-4429-a07f-42c3103d4d01', url: 'https://github.com/majid2709/javaservletlogin.git',branch: 'master'
					     def mvnHome = tool name: 'maven', type: 'maven'
                         def mvnCMD = "/usr/local/src/apache-maven/bin/mvn"
                         sh "${mvnCMD} -f pom.xml clean package"
                }
            }
        }
    }  
                
                 
                 
