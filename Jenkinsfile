pipeline{
    agent any
    tools{
        maven 'M3'
    }
    stages{
		stage('SCM Checkout'){
            steps{
		        git branch: 'master', 
	            credentialsId: 'GitCred',
	            url: 'https://github.com/Dileep9652/MavenTst.git'
			}
		}
        stage("Maven Build"){
            steps{
                bat 'mvn clean package'
            }
        }
        
        }
    }
}