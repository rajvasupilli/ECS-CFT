pipeline {
    agent any 
    stages {
        stage('Create ECS Cluster') {
            steps {
                echo 'Create ECS Resources'
                sh '''
                      aws cloudformation delete-stack --stack-name ecs-stack
                      
                        sleep 30;
                      
                      aws cloudformation create-stack --stack-name ecs-stack --template-body file://create-ecs.yml --capabilities CAPABILITY_IAM
                   '''
            }
        }
    }
}
