pipeline {

    agent {
        node {
            label 'workstation'
        }
    }

    stages {

        stage('One'){
            steps {
                sh 'echo Hello world'
            }
        }
    }

    post {
        always {
            sh 'echo Postcleanup steps'
        }
    }
}