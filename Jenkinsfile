pipeline{
   agent any
    stages{
       stage("Clean Up"){
          steps{
               deleteDir()
          }
       }
       stage("Clone Repo"){
          steps{
            sh " git clone https://github.com/anilkakarla01/maven-demo.git"
          }
       }
       stage("Build"){
           steps{
            dir("maven-demo"){
                sh "mvn clean install"
            }
           }
       }
       stage("Test"){
              steps{
                dir("maven-demo"){
                    sh "mvn test"
                }
              }
       }
    }
}
