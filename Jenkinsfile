pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }
    environment{
        GREETING = 'HELLO JENKINS'
    }
     options {
        timeout(time: 1, unit: 'SECONDS')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                echo 'Deploying....'
                echo '$GREETING'
                """

            }
        }
    }
}