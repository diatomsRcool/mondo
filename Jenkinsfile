pipeline {
	agent none
    stages {
        stage('MergeIfNeeded') {
        	agent {
        		docker {
        			image 'obolibrary/odkfull'
        			args '--memory=8g -e ROBOT_JAVA_ARGS=-Xmx7G -v $PWD:/work -w /work/src/ontology --rm -ti'
        		}
        	}
            steps {
                sh 'make test';
            }
        }
    }
}