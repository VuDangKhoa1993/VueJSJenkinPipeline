pipeline{
    agent {
        docker {
            image 'node:14-alpine'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                sh 'echo 'Kyanon digital ''
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}