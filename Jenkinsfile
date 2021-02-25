pipeline {
    agent any
    environment {
        awsRole = "${env.DEPLOYMENT_ROLE}"
    }
    stages {
        stage('Validating template') {
            steps {
                echo 'Building..'
                //sh "cfn-lint validate EC2Deployment.yml"
                sh 'aws s3 ls'
            }
        }
        stage('Upload CFT to S3') {
            steps {
                withAWS(role:"${awsRole}", roleSessionName:"test") {
                    sh 'aws s3 ls'                
                }
            }
        }
        stage('Deploy CFT') {
            steps {
                echo 'Testing..'
            }
        }       
    }
}