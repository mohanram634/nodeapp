pipeline {
    agent any 
    stages{
        stage('Build the docker Image'){
            steps{
                sh 'docker build . -t mohanram634/nodeapp:v1'
            }
        }

        stage('Push the Image'){
            steps{
                withCredentials([string(credentialsId: 'docker_hub', variable: 'docker')]) {
                sh 'docker login -u mohanram634 -p ${docker}'
                sh 'docker push mohanram634/nodeapp:v1'
                }
            }

        }

        
    }
}
