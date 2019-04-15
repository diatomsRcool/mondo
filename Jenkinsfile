pipeline {
	agent none
    stages {
        stage('Hello') {
            agent any
            steps {
                sh 'env; echo Hello Stage again 6';
                sh 'pwd; ls -la'
            }
        }
    }
}