pipeline {
	agent Linux-node
	stages {
		stage('---clean---'){
			steps {
				tool name: 'maven 3.8.6', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'maven 3.3.3', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'mvn 3.8.1', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
