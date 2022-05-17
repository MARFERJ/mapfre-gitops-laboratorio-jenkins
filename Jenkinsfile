pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
	stage('Shell Script Hello') {
	agent { label 'docker-agent' }
            steps {
                sh 'echo "Hello World, from Shell Script"'
            }
        }
	stage('Test ejecución en Pull Request') {
	    when {
		branch "PR-*"
	    }
            steps {
                sh 'echo "Pedro"| bash ejercicio.sh pruebas'
		sh 'echo "secreto"| bash ejercicio.sh prueba'
            }
        }
    }
}