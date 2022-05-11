pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    stages {
	agent { Label docker }
        stage('Script Shell Hello') {
            steps {
                sh 'echo "Hello World"'
            }
        }
    }
}