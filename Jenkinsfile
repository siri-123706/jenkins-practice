pipeline {
     // agent any 
    agent {
        label 'AGENT-1'
    }
   // build
    stages {
        stage('Build') {
            steps {
                script{
                    echo 'Building..'
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