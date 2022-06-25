pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                ssh 'echo "Hello world"'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only successful'
        }
        failure {
            echo 'This will run only failed'
        }
        unstable {
            echo 'This will run only run was marked or unstable'
        }
        changed {
            echo 'This will run only if step Pipeline has changed'
        }
    }
}