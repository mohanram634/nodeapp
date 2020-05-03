pipeline {
    agent any 
   
    stages{
        stage('Build the docker Image'){
            steps{
                sh 'docker build . -t mohanram634/nodeapp:v1'
            }
        }
    }
}

