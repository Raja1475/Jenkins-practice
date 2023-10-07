pipeline {
    agent { node { label 'Agent1'}}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'pwd'
                sh 'echo Jenkins web-hook'
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