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
        stage('sh Hello') {
            steps {
                sh 'echo "Hello World"'
		}	
	}
}