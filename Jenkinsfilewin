pipeline {
    tools{
        jdk 'JAVA_HOME1'
        maven 'MAVEN_HOME'
    }
    agent {label 'winslave'}

    stages {
        stage('git clone') {
            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
            }
        }
         stage('compile') {
            steps {
                bat 'mvn compile'
                echo 'successfully build the code'
            }
        }
         stage('unit testing') {
            steps {
                bat 'mvn test'
                echo 'successfully unit testing done'
            }
        }
         stage('package') {
            steps {
                bat 'mvn package'
                echo 'successfully packeged'
            }
        }
        stage('deployment') {
            steps {
                //bat 'mvn deploy'
                echo 'successfully deployed'
            }
        }
    }
}
