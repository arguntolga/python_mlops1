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
                sh 'python3 --version' 
		sh 'python3 train_r2_fit.py'
		sh 'python3 test_r2_fit.py'
            }
        }
    }
}
