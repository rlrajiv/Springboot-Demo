pipeline {
          agent any 
  tools { 
          maven 'Maven Latest'
          jdk   'JDK8'
        }
  stages{
    stage('Build'){
      steps{
              sh script: 'mvn clean package'
            }
    }
  }
}
