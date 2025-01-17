pipeline {
	agent none
	
    stages {
		
        stage('git clone compile test pkg on linux') {
			tools{
				jdk 'JAVA_HOME'
				maven 'M2_HOME'
			}
			agent {label 'linuxslave'}

            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
				sh 'mvn compile'
                echo 'successfully compiled the code'
				sh 'mvn test'
                echo 'successfully unit testing done'
				sh 'mvn package'
                echo 'successfully packeged'
				
            }
        }
		
		stage('git clone compile test pkg and dploy on win') {
			tools{
				jdk 'JAVA_HOME1'
				maven 'MAVEN_HOME'
			}
			agent {label 'winslave'}

            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
				bat 'mvn compile'
                echo 'successfully compiled the code'
				bat 'mvn test'
                echo 'successfully unit testing done'
				bat 'mvn package'
                echo 'successfully packeged'
				echo 'successfully deployed'
            }
        }
		
    }
}
