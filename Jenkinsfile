pipeline {
    agent any 
    stages {
        stage('Create ECS Cluster') {
            steps {
                echo 'Build, Tag and Push the Docker Image into Docker Hub'
                sh '''
                      aws cloudformation update-stack --stack-name ecs-stack --template-body file://create-ecs-cluster.yml
                   '''
            }
        }
    }
}
