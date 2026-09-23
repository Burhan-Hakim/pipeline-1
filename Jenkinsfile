pipeline {
    agent none
    stages {
        stage('Test') {
            agent { label 'test' }
            steps {
                git branch: 'develop', url: 'https://github.com/Burhan-Hakim/pipeline-1.git'
                sh '''
                    mkdir -p /home/ubuntu/test-deploy
                    cp -r . /home/ubuntu/test-deploy/
                '''
            }
        }
        stage('Prod') {
            agent { label 'prod' }
            steps {
                git branch: 'develop', url: 'https://github.com/Burhan-Hakim/pipeline-1.git'
                sh '''
                    mkdir -p /home/ubuntu/prod-deploy
                    cp -r . /home/ubuntu/prod-deploy/
                '''
            }
        }
    }
}
