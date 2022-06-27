pipeline {
    agent any
    stages{
        stage('Git Clone'){
            steps{
                git branch: 'main', url: 'https://github.com/Midguar11/Jenkins_Docker_Practice.git'
            }
        }
        
        stage('Maven Build'){
            steps{
                sh 'mvn packkage'
            }
        }

        stage('Create DockerImage'){
            steps{
                sh 'docker build -t thetips4you/springboot:latest .'
            }
        }
        
     }
}
