@Library('pipeline-library-demo')_

pipeline {
    agent none
    stages {
        stage('') {
            agent {
                
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Build') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn clean package'
            }
		script{
		 git credentialsId: 'github-pwd', url: 'https://github.com/pkavyasree/simple-java-maven-app.git'
		 def mvnCMD = "/usr/share/maven/bin/mvn"
                 sh "${mvnCMD} -f pom.xml clean package"
		}
        }
    }
}
