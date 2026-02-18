pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java program...'
                bat 'javac Hello.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                bat 'java Hello'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: '*.class'
            echo 'Build Successful and Artifact Archived'
        }
        failure {
            echo 'Build Failed!'
        }
        always {
            echo 'Mini CI Pipeline Completed'
        }
    }
}
