pipeline {
    agent any 
    tools { 
        maven 'Maven 3.5.0' 
        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                   mvn --version
                   java --version
                ''' 
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean deploy -P sonatype-oss-release' 
            }
        }
    }
}
