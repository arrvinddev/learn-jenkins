pipeline {

    agent {
        node {
            label 'workstation'
        }
    }

    triggers { pollSCM('H/2 * * * *') }

    options {
        ansiColor('xterm')
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'who should i say hello to?')
    }

    environment {
        SAMPLE_URL="example.com"
    }

    stages {

        stage('One'){
            steps {
                sh 'echo Hello world'
                sh 'echo Hello Universe'
                sh 'echo ${SAMPLE_URL}'
                sh 'echo PERSON - ${PERSON}'
            }
        }
    }


    post {
        always {
            sh 'echo Postcleanup steps'
        }
    }
}