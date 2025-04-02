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
    }
}
