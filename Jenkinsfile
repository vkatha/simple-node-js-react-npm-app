pipeline{
    agent{
        docker{
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    env{
        CI='true'
    }
    stages{
        stage('Build'){
            steps{
                sh ' npm install'
            }
        }
        stage('Test'){
            steps{
                sh ' echo "Running test stage"'
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}