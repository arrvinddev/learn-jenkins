pipeline {

    agent {
        node {
            label 'workstation'
        }
    }

    triggers { pollSCM('H * * * *') }

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
             input {
                message "Do you Approve?"
                ok "Yes"
             }
            steps {
                sh 'echo Hello world'
                sh 'echo Hello Universe'
                sh 'echo ${SAMPLE_URL}'
                sh 'echo PERSON - ${PERSON}'
            }
        }
        stage('Two'){
            when {
                expression{
                GIT_BRANCH=="origin/test"
                }
            }
            steps{
                sh 'env'
            }
        }
    }


    post {
        always {
            sh 'echo Postcleanup steps'
        }
    }
}