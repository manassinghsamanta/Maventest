pipeline {
    tools{
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }
    agent {label 'linuxslave'}

    stages {
        stage('git clone') {
            steps {
                git 'https://github.com/manassinghsamanta/Maventest.git'
                echo 'git cloned successfully'
            }
        }
         stage('compile') {
            steps {
                sh 'mvn compile'
                echo 'successfully build the code'
            }
        }
         stage('unit testing') {
            steps {
                sh 'mvn test'
                echo 'successfully unit testing done'
            }
        }
         stage('package') {
            steps {
                sh 'mvn package'
                echo 'successfully packeged'
            }
        }
        stage('deployment') {
            steps {
                //sh 'mvn deploy'
                echo 'successfully deployed'
            }
        }
    }
}
