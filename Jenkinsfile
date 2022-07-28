pipeline {
  agent any
  tools {
    maven "maven-stephanie"
  }
  stages {
    stage ('Maven Clean'){
      steps{
        sh 'mvn clean'
      }
    }
    stage ('Maven package') {
      steps{
        sh 'mvn package'
      }
    }
    
    stage ('Docker image build and push'){
            steps{
              withDockerRegistry([ credentialsId: "Docker_creds", url: "https://index.docker.io/v1/" ]){
                sh 'docker build -t stephanieawono86/java_maven-jenkins . -f Dockerfile'
                sh 'docker push stephanieawono86/java-maven-jenkins'
                
                
                
                
                
                
                
                
                
                
                
                
                
              }
            }
            }
              
              
              
              
              
              
              
              
              
              
              
              
  }
}
  
