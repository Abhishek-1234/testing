pipieline{
  agent any
  
  stages{
    stage('Build'){
      steps{
        mvn package
      }
    }
    stage('Deploy'){
      steps{
        deploy contextPath: 'http://localhost:8082/', war: 'mvnwebapp'
      }
    }
    
  }
  
}
