#!groovy

@Library('github.com/ayudadigital/jenkins-pipeline-library@v6.3.0') _

// Initialize global config
cfg = jplConfig('mapfre-gitpos-laboratorio-jenkins', 'bash', '', [email: 'marferj@mapfre.com'], 'main')

pipeline {
    agent any

       stages {
        stage ('Initialize Shared Library') {
            steps  {
                jplStart(cfg)
            }
        }
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