pipeline {
    agent any
	/*tools{
	    jdk 'localJDK'
	}*/
    stages {
	script{
		env.JAVA_HOME="${tool 'localJDK'}"
		//env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
    	}    
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
