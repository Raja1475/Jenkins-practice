pipeline {
    agent { node { label 'Agent1'}}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo "build completed"
        }

        success {
            echo "build is success"
        }

        failure {
            echo "build is failure  "
        }
    }
}