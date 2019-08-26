pipeline {
    agent any
	/*tools{
	    jdk 'localJDK'
	}*/
    stages {
	stage('Build') {
            steps {
                echo 'Building..'
		bat "mvn --version"
                bat "java -version"
		//bat 'mvn clean'
		script{
			env.JAVA_HOME="${tool 'localJDK'}"
			//env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
    		}    
                bat 'mvn clean install'
            }
	}
        stage('Test') {
            steps {
                echo 'Testing..'
		mvn 'test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
