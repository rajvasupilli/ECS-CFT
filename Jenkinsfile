pipeline {
    agent any 
    stages {
        stage('Create ECS Cluster') {
            steps {
                echo 'Create ECS Resources'
                sh '''
                      aws cloudformation update-stack --stack-name ecs-stack --template-body file://create-ecs.yml --capabilities CAPABILITY_NAMED_IAM
                      
                      //sleep 30;
                      
                      //aws cloudformation create-stack --stack-name ecs-stack --template-body file://create-ecs.yml --capabilities CAPABILITY_NAMED_IAM
                   '''
            }
        }
    }
}
