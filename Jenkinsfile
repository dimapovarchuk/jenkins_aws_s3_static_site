pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
              sh "aws configure set region $AWS_DEFAULT_REGION" 
              sh "aws configure set aws_access_key_id $AWS_ACCESS_KEY_ID"  
              sh "aws configure set aws_secret_access_key $AWS_SECRET_ACCESS_KEY"
              sh "aws s3 rm s3://www.dimapovar1991.com/index.html"
              sh "aws s3 cp index.html s3://www.dimapovar1991.com"
            }
        }
    }
}