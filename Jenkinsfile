pipeline {
    agent none
    stages {
        stage('Build') { 
		agent {
			docker { image 'maven:3.8.5-openjdk-17' }
		}
            	steps {
			sh 'mvn --version'
                	sh 'mvn -B -Denforcer.skip=true -DskipTests clean package' 
            	}
        }
	stage('Test') {
		steps {
			sh 'mvn test'
		}
		post {
               	 always {
                   	 junit 'target/surefire-reports/*.xml'
                 }
            }
	}
    }
}
