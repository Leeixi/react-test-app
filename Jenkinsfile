pipeline {
    agent {
        docker {
            image 'ubuntu:latest' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Envirnment'){
            sh 'git --version'
	    echo "Branch: ${env.BRANCH_NAME}"
            sh 'docker -v'
            sh 'printenv'
        }
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
