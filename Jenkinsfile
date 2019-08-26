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
		//java='C:\Program Files\AdoptOpenJDK\jdk-8.0.202.08\bin\java'
		    script{
		    env.JAVA_HOME="${tool 'localJDK'}"
		    env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
		    }
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
