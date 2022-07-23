pipeline{
 agent any
   tools{
   tool name: 'Dev-Maven', type: 'maven'
       }
   stages{
     stage('Build'){
      steps{
      sh 'mvn clean package'
      }
     }
    stage('Test'){
      steps{
         sh 'mvn test'
           }
         }
    stage('Deploy'){
     steps{
        echo '#########DEPLOY JAR########'
        sh 'java -jar /home/jenkins/workspace/STAGE/Jenkins-Pipeline/target/my-app-1.0-SNAPSHOT.jar'
          }
       }
    stage('Deliver'){
     steps{
         sh './jenkins/scripts/deliver.sh'
          }
       }
  }
} 
     
        
