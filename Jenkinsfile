pipeline{

agent any

stages{
     
      stage("Maven Build"){
           when{
                branch "develop"
           }
           steps{
                sh "mvn clean package"

                }
         }
     stage("Sonar analysis"){
           when{
                branch "develop"
           }
           steps{
                echo "perform sonar analysis"

                }
         }
     stage("Dev develop"){
           when{
                branch "develop"
           }
           steps{
                echo "Deploy to development"

                }
         }
     stage("deploy to qa"){
           when{
                branch "qa"
           }
           steps{
                echo "Deploy to qa"

                }
         }
     stage("Deploy to prod"){
           when{
                branch "main"
           }
           steps{
                echo "deploy to production"

                }
         }
     }
  }
