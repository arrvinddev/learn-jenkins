pipeline {

    agent {
        node {
            label 'workstation'
        }
    }

    environment {
        SAMPLE_URL="example.com"
    }

    stages {

        stage('One'){
            steps {
                sh 'echo Hello world'
                sh 'echo Hello Universe'
            }
        }
    }

    post {
        always {
            sh 'echo Postcleanup steps'
        }
    }
}