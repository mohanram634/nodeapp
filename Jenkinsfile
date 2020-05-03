pipeline {
    agent any 
    
    environment{
        DOCKER_TAG = getDockerTag()
    }

    stages{
        stage('Build the docker Image'){
            steps{
                sh 'docker build . -t mohanram634/nodeapp:${DOCKER_TAG}'
            }
        }
    }
}




def getDockerTag(){
    def tag = sh script: 'git rev-parse HEAD',returnStdout: true
    return tag
}
