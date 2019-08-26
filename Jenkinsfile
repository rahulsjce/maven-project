pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		bat "mvn --version"
                bat "java -version"
		//bat 'mvn clean'
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
