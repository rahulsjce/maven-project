pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		bat "mvn --version"
                bat "java -version"
		//bat 'mvn clean'
		java='C:\Program Files\AdoptOpenJDK\jdk-8.0.202.08\bin\java'
                bat 'mvn clean package'
            }
	}
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
