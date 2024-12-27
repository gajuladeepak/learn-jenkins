pipeline {
    agent {
        label 'Agent-1'
    }
    options {
        timeout(time: 10, unit: 'SECONDS')
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
            }
        }
    }

    post{
        always{
            echo "This sections runs always"
            deleteDir()
        }
    }
}