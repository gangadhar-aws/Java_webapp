@Library('my-shared-lib') _

pipeline{
    agent any

    stages{

    // stage 1 Git checkout    
        stage("Git Checkout"){

            steps{
                script{
                    gitCheckout(
                        branch: "main",
                        url: "https://github.com/gangadhar-aws/Java_webapp.git"
                    )
            }   }

        }

    // Stage 2 Unit Test
        stage("Maven Unit Test"){   

            steps{
                script{
                     mvnTest()
                }   
            }

        }

    // Integration Test
          stage("Maven Integration Test"){   

            steps{
                script{
                    //mavenIntegration()
                    sh 'echo integration test going on ...assume...'
                }   
            }

        }








    }
}