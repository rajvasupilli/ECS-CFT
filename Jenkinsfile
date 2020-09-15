pipeline {
    agent any 
    stages {
        stage('Create ECS Cluster') {
            steps {
                echo 'Build, Tag and Push the Docker Image into Docker Hub'
                sh '''
                      aws cloudformation delete-stack --stack-name ecs-stack
                      aws cloudformation create-stack --stack-name ecs-stack --template-body file://create-ecs.yml
                   '''
            }
        }
    }
}
