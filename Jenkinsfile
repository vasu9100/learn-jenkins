pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello, world!'
            }
        }

        stage('Hi') {
            steps {
                echo "Hi How are you"
            }
        }
    }

    post {

        always {
            echo "I will say Hi To you I respective of your pipe line status"
        }

        success {
            echo "I will say Hi to you when ever ur pipe line runs successfully"

        }

        failure {
            echo "I will say hello when ever your pipeline got failed"
        }
    }
}
