pipeline{
    agent {
        docker {
            image 'node:14-alpine'
        }
    }
    stages {
        stage('build') {
            steps {
               bat 'set'
               echo 'the build is running'
            }
        }
        stage('Test') {
            steps {
                echo 'Fail! exit 1 '
            }
        }
    }
    post {
        always {
            echo 'This is always run'
        }
        success {
            echo 'This will only run if successfully'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only when the run was marked as unstable' 
        }
        changed {
            echo 'This will run only when the state of the pipeline has changed'
            echo 'For example, if the previous state was failing but is now successfully'
        }
    }
}