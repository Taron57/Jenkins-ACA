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
                    sh "docker run -tid -p 2222:80 my-image:${env.BUILD_ID}"
//docker.image("my-image:${env.BUILD_ID}").withRun('-p 2222:80') {
//* do things */
//                        }
                  }  
             }
        }
    }
}