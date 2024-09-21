pipeline{
    
    agent any
    tools{
        maven 'mymaven'
    }
    stages{
        stage('Clone Repo'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Compile Code'){
            steps{
                sh 'mvn compile'
            }
        }
         stage('Review Code'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
         stage('Test Code'){
            steps{
                sh 'mvn test'
            }
        }
         stage('Package Code'){
            steps{
                sh 'mvn package'
            }
        }
    }
    
}
