pipeline {
    agent any
    environment {
        BRANCH = "${BRANCH_NAME}"
        APPSCOPE = 'rhino.global'
        CREDENTIALS = 'PartyReadySN'
        TESTENV = 'https://dev104977.service-now.com/'
    }

    stages {
        stage('preparation') {
            steps {
                echo "Pipeline is running" // for debugging
                snApplyChanges(appScope: "${APPSCOPE}", branchName: "${BRANCH}", url: "${TESTENV}", credentialsId: "${CREDENTIALS}")
            }
        }
    }
}
