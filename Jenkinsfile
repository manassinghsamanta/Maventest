pipeline {
	agent none
	
    stages {
		tools{
				jdk 'JAVA_HOME'
				maven 'M2_HOME'
			}
			agent {label 'linuxslave'}
        stage('clone') {
			

            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
            }
			}
		stage('compile') {	
			steps {
				sh 'mvn compile'
                echo 'successfully compiled the code'				
            }
		}
		stage('test') {
			steps {
				sh 'mvn test'
                echo 'successfully unit testing done'				
            }
		}
		stage('package') {
			steps {
				sh 'mvn package'
                echo 'successfully packaged'				
            }
        }
		
		
		
		
    }
}
