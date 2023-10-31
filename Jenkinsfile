pipeline {
    agent any
    tools {
        // Specify the Maven tool name directly (e.g., 'Maven 3.8.1')
         maven 'Maven 3.8.1'
    }
    stages {
        stage('maven clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('maven install') {
            steps {
                sh 'mvn install'
            }
        }
        stage('maven package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
