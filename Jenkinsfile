pipeline {
    agent any
    environment {
        BRANCH = "${BRANCH_NAME}"
        APPSYSID = 'edf27aa21ba0011045706464604bcb38'
        CREDENTIALS = 'PartyReadySN'
        TESTENV = 'https://dev57324.service-now.com//'
    }

    stages {
        stage('preparation') {
            steps {
                echo "Pipeline is running" // for debugging
                snApplyChanges(appSysId: "${APPSYSID}", branchName: "${BRANCH}", url: "${TESTENV}", credentialsId: "${CREDENTIALS}")
            }
        }
    }
}
