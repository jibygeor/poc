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
                input('Do you want to proceed?')
         echo 'Testing....'
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
