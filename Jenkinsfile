pipeline {
    agent any
    
    environment{
    AWS_DEFAULT_REGION = 'us-east-1'
    AWS_CREDENTAILS=credentials('aws_credentials')
    }
    
    stages {
        stage('aws-test') {
            steps {
             //* withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws_credentials', \
              secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]){ *// if below commands doesn't have access put within this block
                    sh'''
                    aws --version
                    aws ec2 describe-instances
                 '''
        }
    }
}
}
