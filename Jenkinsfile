pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }

    options {
        timeout (time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello, world!'
            }
        }

        stage('Hi') {
            steps {
                sh """
                    echo "Hi Slepping running"
                    sleep 10
                """
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
