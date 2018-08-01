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
    agent { docker { image 'node:6.14' } }
    stages {
        stage('build') {
            steps {
                echo "Testing NPM Version"
                sh 'npm --version'
                
            }
        }
    }
}
