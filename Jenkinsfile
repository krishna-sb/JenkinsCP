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
                sh 'docker run --rm -p 7080:8080 tomcat:8.0 &'
            }
            
        }
        stage('Run Tomcat') {
            steps {
                echo "Path: $PATH"
                //sh 'docker run -it --rm -p 7080:8080 tomcat:8.0'
                sh "curl localhost:7080"
            }
            
        }
    }
}
**/


node {
    
        stage('build') {

                echo "Testing tomcat Version"
        
        }
        stage('deploy) {
             sh 'docker build -t "testpipe:dockerfile" /Users/ksubbian/Documents/Anaconda/Jenkins'
             
        }
        stage('Run Tomcat') {
                sh 'docker rm -f "testpipe"'
                echo "Path: $PATH"
                sh 'docker run --name "testpipe" -d --rm -p 7080:8080 testpipe:dockerfile'   
        }
    
        stage('Test Tomcat') {

                sh 'sleep 20' 
                sh "curl http://localhost:7080/UserManagement/rest/Employees | json_pp"

            
        }


}


