pipeline {
     // agent any 
    agent {
        label 'AGENT-1'
    }
    environment {
        COURSE = 'jenkins'

    }
    options { // pipeline expries 30 mint
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds() // not parallel to pipelines at a time so, one complted after another complted
    }
   // build
    stages {
        stage('Build') {
            steps {
                script{
                   // echo 'Building..'
                   sh """
                   echo "hello world"
                   sleep 10
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