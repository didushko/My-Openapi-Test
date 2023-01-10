pipeline {
    agent { label 'slave' }

    stages {
        stage('Audit OpenAPI files') {
            steps {
                sh 'printenv'
                audit repositoryName: "${env.GIT_URL}", branchName: "${env.BRANCH_NAME}", credentialsId: 'platform-dev-anton-test', platformUrl: 'https://platform.dev.42crunch.com', logLevel: 'DEBUG', shareEveryone: 'OFF', jsonReport: "test.json", skipLocalChecks: true
            }
        }
    }
}
