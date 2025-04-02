pipeline {
    agent none
    stages {
        stage('Build') { 
		agent {
			docker { image 'maven:3.8.1-adoptopenjdk-11' }
		}
            	steps {
			sh 'mvn --version'
                	sh 'mvn -B -DskipTests clean package' 
            	}
        }
    }
}
