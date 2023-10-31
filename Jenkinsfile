   pipeline{
    agent any 
    tools{
         maven 'https://dlcdn.apache.org/maven/maven-3/3.9.5/binaries/apache-maven-3.9.5-bin.tar.gz'
    }
    stages{
    stage('maven clean'){
        steps{
        sh  'mvn clean'
        }
    }
    stage('maven install'){
        steps{
          sh  'mvn install'
            
        }
    }
    stage('maven package'){
        steps{
         sh   'mvn package'
        }
    }
   stage('upload artifact'){
        steps{
            nexusArtifactUploader artifacts: [[artifactId: 'bioMedical',
             classifier: '',
              file: 'target/bioMedical-0.0.2-SNAPSHOT.jar', 
              type: 'jar']], 
              credentialsId: 'NexusID',
               groupId: 'qa',
                nexusUrl: '198.58.119.40:8081',
                 nexusVersion: 'nexus3',
                  protocol: 'http', 
                  repository: 'prof-repo',
                   version: '002'
        }
    }

    }

}
    