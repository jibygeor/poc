pipeline {
    agent any

    stages {
        stage('Build') {
           input{
                     message "Press Ok to continue"
                     submitter "user1,user2"
                     parameters {
                     string(name:'username', defaultValue: 'user', description: 'Username of the user pressing Ok')
                    }
                }
        steps { 
            echo "User: ${username} said Ok."
        }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
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
