pipeline {
    agent any

    stages {
        stage('Build') {
           steps { 
         echo 'Building'
           }
        }
        stage('Test') {
            steps {
                inpt=  input "Approve/deny Testing to production system"
                echo 'Testing status $inpt'
            }
        }
        stage('Deploy') {
           
            steps {
               //  timeout(time: 20, unit: 'SECONDS') {
               
             //}
                echo 'Deploying....'
            }
        }
    }
    /* post {
        always {
            echo 'Done'
        }
        failure {
            echo ':('
        }
         success {
            echo ':)' 
        }
    } */
}
