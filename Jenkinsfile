pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'frolvlad/alpine-python-machinelearning' 
                }
            }
            steps {
                sh 'python --version' 
		sh 'python train_r2_fit.py'
            }
        }
    }
}
