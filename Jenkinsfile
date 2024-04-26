pipeline {

    agent {
        node {
            label 'workstation'
        }
    }

    options {
        ansiColor('xterm')
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
            }
        }
    }

    post {
        always {
            sh 'echo Postcleanup steps'
        }
    }
}