pipeline {
    agent any
    stages {
        stage ('Stage  1') {
            steps {
                bat 'echo this is the first Jenkins job'
            }
        }
    }
    post {
        always {
            echo 'This step will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will only run if the run was makred as unstable'
        }
        changed {
            echo 'This will only run if the State of Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}