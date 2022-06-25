pipeline {
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello world"'
                sh '''
                    'echo "Multiline shell steps works too"'
                    ls -lah
                '''
            }
        }
    }
}