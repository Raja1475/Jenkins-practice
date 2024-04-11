pipeline {
    agent { node { label 'agent1' }}

    stages {
        stage ('build') {
            steps {
                echo "building..."
                sh '''
                pwd
                ls -lrt
                '''
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