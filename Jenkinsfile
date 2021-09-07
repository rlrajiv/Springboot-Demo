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
  }
}
