pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'python --version' 
		sh 'python train_r2_fit.py'
            }
        }
    }
}
