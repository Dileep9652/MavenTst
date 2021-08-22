pipeline{
    agent any
    tools{
        maven 'M3'
    }
    stage('SCM Checkout'){
        git branch: 'master', 
	        credentialsId: 'GitCred',
	        url: 'https://github.com/Dileep9652/MavenTst.git'
    }
    stage('Maven Build'){
        def mvnHome = tool name: 'M3', type: 'maven'
		sh "${mvnHome}/bin/mvn clean package"
    }
}