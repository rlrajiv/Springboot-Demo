pipeline {
          agent any 
  tools { 
          maven 'Maven Latest'
         }
  stages{
    stage('Build'){
      steps{
              sh script: 'mvn clean package'
            }
        }
                         
    stage('Upload War to nexus'){
      steps{
              nexusArtifactUploader artifacts: [[artifactId: 'SpringBootMavenExample', classifier: '', file: 'target/SpringBootMavenExample-1.3.7.RELEASE.war', type: 'war']], 
                        credentialsId: 'jeknins-nexus', groupId: 'org.springframework.boot', nexusUrl: '162.248.163.127:8081/nexus', nexusVersion: 'nexus3', protocol: 'http', repository: 'springboot-demo-release', version: '1.3.7.RELEASE'
            }
    }
   }           
  }
