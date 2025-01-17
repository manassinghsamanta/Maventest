pipeline {
	agent none
	
    stages {
		
        stage('linux') {
			tools{
				jdk 'JAVA_HOME'
				maven 'M2_HOME'
			}
			agent {label 'linuxslave'}

            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
            }
			steps {
				sh 'mvn compile'
                echo 'successfully compiled the code'				
            }
			steps {
				sh 'mvn test'
                echo 'successfully unit testing done'				
            }
			steps {
				sh 'mvn package'
                echo 'successfully packaged'				
            }
        }
		
		stage('win') {
			tools{
				jdk 'JAVA_HOME1'
				maven 'MAVEN_HOME'
			}
			agent {label 'winslave'}

            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
            }
			steps {
				bat 'mvn compile'
                echo 'successfully compiled the code'
            }
			steps {
				bat 'mvn test'
                echo 'successfully unit testing done'
            }
			steps {
				bat 'mvn package'
                echo 'successfully packeged'
            }
			steps {
				echo 'successfully deployed'
            }
        }
		
    }
}
