@Library('my-shared-lib') _

pipeline{
    agent any

    stages{

        stage("Git Checkout"){

            steps{
                script{
                    gitCheckout(
                        branch: "main",
                        url: "https://github.com/gangadhar-aws/Java_webapp.git"
                    )
            }   }

        }

    }
}