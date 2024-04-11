pipeline {
    agent { node { label 'agent1' }}

    stages {
        stage ('build') {
            steps {
                echo "building..."
            }
        }

        stage ('test') {
            steps {
                echo "testing..."
            }
        }

        stage ('Deploy') {
            steps {
                echo "deploying"
            }
        }
    }

    post {
        always {
            echo "build comples"
        }
        success {
            echo "pipeline success"
        }
        failure {
            echo "pipeline failure"
        }
    }
}