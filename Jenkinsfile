pipeline {
    agent none
    stages {
        stage('Build') { 
		agent {
			docker { image 'maven:3.9.2-adoptopenjdk-17' }
		}
            	steps {
			sh 'mvn --version'
                	sh 'mvn -B -DskipTests clean package' 
            	}
        }
    }
}
