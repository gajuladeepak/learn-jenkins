pipeline {
    agent {
        label 'Agent-1'
    }
    options {
        timeout(time: 10, unit: 'SECONDS')
        disableConcurrentBuilds()
        retry(1)
    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo this is build'
                sh 'sleep 10'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo this is build'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo this is build'
                error 'pipeline failed'
            }
        }
    }

    post {
        always{
            echo "This sections runs always"
            deleteDir()
        }
    }
}