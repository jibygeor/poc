pipeline {
    agent any

    stages {
        stage('Build') {
           steps { 
         echo 'Building'
           }
        }
        stage('Test') {
           def userInput = input(
 id: 'userInput', message: 'Let\'s promote?', parameters: [
 [$class: 'TextParameterDefinition', defaultValue: 'uat', description: 'Environment', name: 'env']
])
echo ("Env: "+userInput)
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
