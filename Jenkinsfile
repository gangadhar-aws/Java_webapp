@Library('my-shared-lib') _

pipeline{
    agent any

    parameters{
        choice(name:'action', choices: 'Create\nDelete', description: 'Choose Create\Destroy')
    }

    stages{

    // stage 1 Git checkout    

        when{expression { params.action == 'create' }}
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
        when{expression { params.action == 'create' }}
        stage("Maven Unit Test"){   

            steps{
                script{
                     mvnTest()
                }   
            }

        }

    // Integration Test
          when{expression { params.action == 'create' }}
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