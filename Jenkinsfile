pipeline {
    agent any
    stages {
        stage ('SCM for Java Code test') {
            steps{
                git changelog: false, url: 'https://github.com/jabedhasan21/java-hello-world-with-maven'
                echo 'Polling to Developers SCM'
            }
        }
        stage ('Maven Compile') {
            steps{
                sh '''mvn clean
mvn compile'''
            }
        }
        stage ('Testing Code') {
            steps {
                sh '''mvn test'''
                echo 'Testing complete with Junit on maven'

            }
        }
        stage ('Package') {
            steps {
            sh 'mvn package'   
            }
        }
    }
}
