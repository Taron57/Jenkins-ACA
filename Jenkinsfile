pipeline {
    agent any 
    stages {
        stage('Build') { 
            script {
                    def customImage = docker.build("my-image:${env.BUILD_ID}")
                }
            }
        
        }
    }
}