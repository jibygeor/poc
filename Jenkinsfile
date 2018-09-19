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
            timeout(time: 1, unit: 'WEEK') {
                 input "Approve/deny deployment to production system"
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
