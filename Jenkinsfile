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
                def doesJavaRock = input(message: 'Do you like to Test?', ok: 'Yes', 
                        parameters: [booleanParam(defaultValue: true, 
                        description: 'If you like to Test, just push the button',name: 'Yes?')])

                echo "Test rocks?:" + doesJavaRock
                
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
