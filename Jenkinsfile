pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy'
            }
        }
    }
    post {
        always {
            echo "This section runs always"
        }
        success {
            echo "This section runs if pipeline is success"
        }
        failure {
            echo "This section runs if pipeline is failed"
        }
    }
}