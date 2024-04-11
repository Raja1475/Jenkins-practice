pipeline {
    agent { node { label 'agent1' }}

    options {
        ansiColor('xterm')
    }

    parameters {
        string(name: 'BRANCH', defaultValue: 'master', description: 'Branch name')
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Deploy application?')
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'production'], description: 'Select environment')
        file(name: 'CONFIG_FILE', description: 'Upload configuration file')
    }

    stages {
        stage('Example') {
            steps {
                echo "Branch: ${params.BRANCH}"
                echo "Deploy: ${params.DEPLOY}"
                echo "Environment: ${params.ENVIRONMENT}"
                echo "Config File: ${params.CONFIG_FILE}"
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