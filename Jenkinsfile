pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
	stage('Shell Script Hello') {
	agent { Label 'docker-agent' }
            steps {
                sh 'echo "Hello World, from Shell Script"'
            }
        }
    }
}