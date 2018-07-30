/* pipeline {
    agent any
    stages {
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
    agent { docker { image 'node:6.3' } }
    environment {
        PATH = "/usr/local/bin:$PATH"
    }
    stages {
        stage('build') {
            steps {
                sh 'echo $PATH'
                sh 'npm --version'
                
            }
        }
    }
}
