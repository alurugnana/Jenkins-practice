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
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
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
                # sleep 10
                """

            }
        }
    }
}