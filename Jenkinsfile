node{

    stage('SCM Checkout'){
    git credentialsId: 'github-pwd', url: 'https://github.com/pkavyasree/simple-java-maven-app.git'
    }
    stage('Mvn Package'){
         def mvnHome = tool name: 'maven', type: 'maven'
         def mvnCMD = "/usr/share/maven/bin/mvn"
         sh "${mvnCMD} -f pom.xml clean package"
     } 
    stage('output'){
        sh label: '', script: 'echo  " This Job $JOB_NAME is succesful and its build number is $BUILD_NUMBER ." '
    }
}
