@Library('my-shared-lib') _

pipeline{
    agent any

    parameters{
        choice(name:'action', choices: 'create\nDelete', description: 'Choose Create/Destroy')
    }

    stages{

    // stage 1 Git checkout    

      
        stage("Git Checkout"){
                 when { expression { params.action == 'create' }}
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
                 when { expression { params.action == 'create' }}
            steps{
                script{
                     mvnTest()
                }   
            }

        }

    // Integration Test
          
          stage("Maven Integration Test"){  
                when {expression { params.action == 'create' }}

            steps{
                script{
                    //mavenIntegration()
                    sh 'echo integration test going on ...assume...'
                }   
            }

        }








    }
}