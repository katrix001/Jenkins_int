pipeline {
    agent { label 'aws'}

    options {

        buildDiscarder(logRotator(daysToKeepStr: '10', numToKeepStr: '10'))

        timeout(time: 12, unit: 'HOURS')

        timestamps()
    }

    triggers {
        cron '@midnight'
    }

    stages{
        stage ('Requirements') {
            steps {
                echo 'Installing requirements..!'
            }
        }
        stage ('Build') {
            steps {
                echo 'Building..!'
            }
        }
        stage ('Test') {
            steps {
                echo 'Testing..!'
            }
        }
        stage ('Report') {
            echo 'Reporting..!'
        }
    }

    post {
        always {
            echo 'This step will run after all other steps have completed.'
        }
    }
}