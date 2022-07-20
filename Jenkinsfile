pipeline {
    agent any
    stages{
        stage('Git Clone'){
            steps{
                git branch: 'main', url: 'https://github.com/Midguar11/Jenkins_Docker_Practice.git'
            }
        }
        
        stage('maven build'){
            steps{
                sh 'mvn package'
            }
        }

        stage('Create DockerImage'){
            agent { 
                label 'DockerAgent01'
            }
            steps{
                sh 'docker build -t midguard/springboot:latest .'
            }
        }
        
     }
}
