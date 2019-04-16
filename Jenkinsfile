pipeline {
	agent none
    stages {
        stage('MergeIfNeeded') {
        	agent {
        		docker {
        			image 'obolibrary/odkfull'
        			args '--memory=8g -e ROBOT_JAVA_ARGS=-Xmx7G'
        		}
        	}
            steps {
                	sh 'cd /var/lib/jenkins/workspace/test-mondo/src/ontology; make test';
            }
        }
    }
}