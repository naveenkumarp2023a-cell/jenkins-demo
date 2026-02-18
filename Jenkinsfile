pipeline {
    agent any

    stage('Build') {
    steps {
        error "Forcing build failure"
    }
}


        stage('Test') {
            steps {
                echo 'Testing project...'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
