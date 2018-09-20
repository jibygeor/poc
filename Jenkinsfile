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
               parallel {
                stage('On Windows') {
                  
                    steps {
                        echo 'Deploying....'
                    }
                    post {
                        always {
                             echo 'Done....'
                        }
                    }
                }
                stage('On Linux') {
                   
                    steps {
                        echo 'Deploying....'
                    }
                    post {
                        always {
                            echo 'Done....'
                        }
                    }
                }
            }
               
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
