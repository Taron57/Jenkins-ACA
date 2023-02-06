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
        stage('Run step') { 
            steps {
                script {
                        docker.image("my-image:${env.BUILD_ID}").withRun('-p 1234:80') {
                            /* do things */
                        }
             }   }
        }
    }
}