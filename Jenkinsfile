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
    environment {
        PATH = "/usr/local/bin:$PATH"
    }
    agent { label 'docker' }
    stages {
        stage('build') {
            steps {
                sh 'echo $PATH'
                sh 'java -version'
                
            }
        }
    }
}
