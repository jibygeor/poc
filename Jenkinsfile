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
