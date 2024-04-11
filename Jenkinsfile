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
            echo "build completed"
        }
        success {
            echo "pipeline success done"
        }
        failure {
            echo "pipeline failure"
        }
    }
}