
pipeline{
    agent any
    tools{
        maven 'M3'
    }
    stages{
        stage("Create Folder"){
            steps{
                sh "mkdir -p ${env.JOB_NAME}"
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

