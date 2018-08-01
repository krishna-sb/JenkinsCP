/* pipeline {
    agent any
    stages {
    { docker { image 'node:6.3' } }
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh 'python --version'
                sh 'java -version'
            }
        }
    }
}*/

/**
pipeline {
    agent { docker { image 'tomcat:8.0' } }
    stages {
        stage('build') {
            steps {
                echo "Testing tomcat Version"
                
            }
            
        }
        stage('Run Tomcat') {
            steps {
                echo "Path: $PATH"
                //sh 'docker run -it --rm -p 7080:8080 tomcat:8.0'
                sh "curl localhost:8080"
            }
            
        }
    }
}
**/

node {
    
    
        stage('build') {

                echo "Testing tomcat Version"
                

            
        }
        stage('Run Tomcat') {

                echo "Path: $PATH"
                sh 'docker run --rm -p 7080:8080 tomcat:8.0 &'
                sh 'sleep 20' 
                sh "curl localhost:7080"

            
        }

}

