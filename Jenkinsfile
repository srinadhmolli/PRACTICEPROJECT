pipeline{ 
   agent any
  
  environment{
    PATH ="/opt/maven3/bin:$path" 
 }
  stages{
    stage (git checkout){
       steps{
          git credentialsId: 'javahome2', url: https://github.com/srinadhmolli/PRACTICEPROJECT.git
        }
    }
    stage ("maven bulid"){
      steps{
          sh"mvn clean package"
          sh"mv target/*.war target/myweb.war"
        }
     }
   }
 }
