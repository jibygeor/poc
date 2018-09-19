pipeline {
    agent any

    stages {
        stage('Build') {
        steps { 
            echo "Starting checkout"
        }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            input{
                     message "Please confirm to continue"
             
                }
            steps {
                echo 'Deploying....'
            }
        }
    }
     post {
        always {
            echo 'Done'
        }
        failure {
            echo ':('
        }
         success {
            echo ':)' 
        }
    }
}
