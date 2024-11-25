pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('Build') {
            options {
                // Timeout counter starts BEFORE agent is allocated
                timeout(time: 10, unit: 'SECONDS')
            }
            steps {
                sh 'echo This is build'
                // sh 'sleep 11'
            }
        }
        stage('Test') {
             options {
                // Timeout counter starts BEFORE agent is allocated
                timeout(time: 10, unit: 'SECONDS')
            }
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
            deleteDir() 
        }
        success {
            echo "This section runs if pipeline is success"
        }
        failure {
            echo "This section runs if pipeline is failed"
        }
    }
}