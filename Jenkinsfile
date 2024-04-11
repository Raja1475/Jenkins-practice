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

        stage ('apply') {
            steps {
                 timeout(time: 15, unit: "MINUTES") {
	                    input message: 'Do you want to approve the deployment?', ok: 'Yes'
	                }

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