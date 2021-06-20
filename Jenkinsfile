pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                bat 'mvn package'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing'
            }
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat6(credentialsId: '8bc53fec-e8b9-4cd7-89f1-091d75c44141', path: '', url: 'http://localhost:8082/')], contextPath: 'mvnwebapp', war: '**/*.war'
            }
        }
    }
}
