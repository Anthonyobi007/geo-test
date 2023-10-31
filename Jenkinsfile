pipeline{
    agent any
    stages {
    stage('maven clean'){
        steps{
            sh 'mvn clean'
        }
    }
   stage('maven install'){
    steps{
        sh 'install'

    }
   }
   stage('maven package'){
    steps{
        'mvn package'
    }
   }

}

}