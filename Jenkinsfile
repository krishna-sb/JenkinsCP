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
                sh 'docker run -it --rm -p 7080:8080 tomcat:8.0'
            }
            
        }
    }
}
