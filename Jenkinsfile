pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
            script{
			env.JAVA_HOME="${tool 'localJDK'}"
			} 
            steps {
                withMaven(maven : 'localMaven') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'localMaven') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}
