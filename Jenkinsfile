@Library('Shared') _
pipeline {
    agent {label 'dev'}

    stages {
        stage('Cloning') {
            steps {
                script{
                    
                cloneRepo('https://github.com/akash-biswas-dev/DemoCI.git','main')
                }
            }
        }
        stage('Push to Docker'){
            steps{
                script{
                    dockerPush("dockerHub")
                }
            }
        }
    }
}
