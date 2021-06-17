pipieline{
  agent any
  
  stages{
    stage('Build'){
      steps{
        echo 'building maven based project'
        mvn package
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploying webpage to tomcat'
        deploy contextPath: 'http://localhost:8082/', war: 'mvnwebapp'
      }
    }
    
  }
  
}
