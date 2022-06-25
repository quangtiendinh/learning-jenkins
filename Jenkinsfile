pipeline {
    agent any
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
            deleteDir() // clean up workspaces
        }
        success {
            echo 'This will run only successful'
            mail to: 'dinhquangtien0169@gmail.com',
                 subject: "The Pipeline ${currentBuild.fullDisplayName}",
                 body: "The Pipeline ${currentBuild.fullDisplayName} completed successful"
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