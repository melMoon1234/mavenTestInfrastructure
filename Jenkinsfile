pipeline {
    agent any
    stages {
        stage('Validating template') {
            steps {
                echo 'Building..'
                sh "cfn-lint EC2Deployment.yml"
            }
        }
        stage('Upload CFT to S3') {
            steps {
                echo 'Building..'
            }
        }
        stage('Deploy CFT') {
            steps {
                echo 'Testing..'
            }
        }       
    }
}