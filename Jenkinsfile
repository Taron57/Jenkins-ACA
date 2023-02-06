pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                script {
                        def customImage = docker.build("my-image:${env.BUILD_ID}")
                    }
            }
        
        }
    }
}