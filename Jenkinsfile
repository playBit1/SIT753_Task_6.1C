pipeline {
    agent any
    environment{
        PROJECT_NAME = "Task 6.1 Pipeline"
    }
    stages{
        stage("Build"){
            steps{
                echo "Running Maven build..."
                echo "Compiling source code..."
                echo "Packaging application..."
                echo "Build successful!"
                echo "Tool Used: Maven"
            }
        }
        stage("Unit and Integration Tests"){
            steps{
                echo "Running unit tests with JUnit..."
                echo "Test case 1: Sample flow... PASSED"
                echo "Unit tests passed!"
                echo "Running integration tests with Selenium..."
                echo "Test case 1: Sample flow... PASSED"
                echo "Integration tests passed!"
                echo "Tool Used: JUnit (Unit Testing), Selenium (Integration Testing)"
            }
            post{
                success{
                    emailext to: "binulben5@gmail.com",
                    subject: "$PROJECT_NAME - Build Successful!",
                    body: "The build was successful on the Testing stage!",
                    attachLog: true
                }
                failure{
                    emailext to: "binulben5@gmail.com",
                    subject: "$PROJECT_NAME - Build Failed!",
                    body: "The build Failed on the Testing stage!",
                    attachLog: true
                }
            }
        }
        stage("Code Analysis"){
            steps{
                echo "Analyzing code with SonarQube..."
                echo "Code analysis complete."
                echo "Tool Used: SonarQube"
            }
        }
        stage("Security Scan"){
            steps{
                echo "Scanning code for vulnerabilities with OWASP ZAP..."
                echo "Security scan complete."
                echo "Tool Used: OWASP ZAP"
            }
            post{
                success{
                    emailext to: "binulben5@gmail.com",
                    subject: "$PROJECT_NAME - Build Successful!",
                    body: "The build was successful on the Security Scan stage!",
                    attachLog: true
                }
                failure{
                    emailext to: "binulben5@gmail.com",
                    subject: "$PROJECT_NAME - Build Failed!",
                    body: "The build Failed on the Security Scan stage!",
                    attachLog: true
                }
            }
        }
        stage("Deploy to Staging"){
            steps{
                echo "Deploying the application to a staging server"
                echo "Tool Used: AWS CodeDeploy"
            }
        }
        stage("Integration Tests on Staging"){
            steps{
                echo "Starting integration tests on staging environment..."
                echo "Test case 1: Sample flow... PASSED"
                echo "Integration tests passed!"
                echo "Tool Used: Selenium"
            }
        }
        stage("Deploy to Production"){
            steps{
                echo "Starting deployment to production server..."
                echo "Deploying version of the application to production..."
                echo "Deployment to production successful!"
                echo "Tool Used: AWS CodeDeploy"
            }
        }
    }
}