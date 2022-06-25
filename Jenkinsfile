pipeline {
    agent {
        docker { image: 'node:16.13.1-alpine'}
    }
    stages {
        stage ('Build') {
            steps {
                sh 'echo "Hello world"'
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