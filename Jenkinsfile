pipeline {
     // agent any 
    agent {
        label 'AGENT-1'
    }
    environment {
        COURSE = 'jenkins'

    }
   // build
    stages {
        stage('Build') {
            steps {
                script{
                   // echo 'Building..'
                   sh """
                   echo "hello world"
                   env
                   """
                }
                
            }
        }
        stage('Test') {
            steps {
                script{
                    echo 'Testing..'
                }
                
            }
        }
        stage('Deploy') {
            steps {
                script{
                    echo 'Deploying....'
                }
                
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir() // delete post build pipeline in workspace  
        }
        success { 
            echo 'hello success'
        }
        failure { 
            echo 'hello failure'
        }
    }

}