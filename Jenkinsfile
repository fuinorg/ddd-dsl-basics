pipeline {
    agent any 
    tools { 
        maven 'Maven (latest)' 
        jdk 'Oracle JDK 1.8 (latest)'
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
