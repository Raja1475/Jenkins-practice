pipeline {
    agent { node { label 'agent1' }}

    options {
        ansiColor('xterm')
    }

    stages {
        stage ('init') {
            steps {
                sh 'terraform init'
            }
        }

        stage ('plan') {
            steps {
                sh 'terraform plan'
            }
        }

        stage ('approval') {
            input {
                message "terraform apply?"
            }
        }

        stage ('apply') {
            steps {
                sh 'terraform apply -auto-approve'
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