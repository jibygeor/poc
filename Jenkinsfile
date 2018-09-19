pipeline {
    agent any

    stages {
        stage('Build') {
        parallel (
            "First Build" : {
                echo 'first-build-job'
            },
            "Second Build" : {
                echo 'second-build-job'
            }
        )
        build("test-job")
        parallel (
            "Third Build" : {
                echo 'third -build-job'
            },
            "Last Build" : {
                 echo 'last-build-job'
            }
        )
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
           
            steps {
               //  timeout(time: 20, unit: 'SECONDS') {
                 input "Approve/deny deployment to production system"
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
