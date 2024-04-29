pipeline {
    agent any
    environment {
        DIRECTORY_PATH = "C:\\Users\\Binul\\Projects\\Task5.1"
        TESTING_ENVIRONMENT = "Performance Testing Environment"
        PRODUCTION_ENVIRONMENT = "Binul"
    }
    stages{
        stage("Build"){
            steps{
                echo "fetch the source code from $DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
        }
        stage("Test"){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage("Code Quality Check"){
            steps{
                echo "check the quality of the code"
            }
        }
        stage("Deploy"){
            steps{
                echo "deploy the application to $TESTING_ENVIRONMENT"
            }
        }
        stage("Approval"){
            steps{
                sleep 10
            }
        }
        stage("Deploy to Production"){
            steps{
                echo "Deploying the code to production environment: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}