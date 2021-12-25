pipeline {
    agent any
    environment {
        BRANCH = "${BRANCH_NAME}"
        APPSYSID = 'edf27aa21ba0011045706464604bcb38'
        CREDENTIALS = 'PartyReadySN'
        TESTENV = 'https://dev104977.service-now.com/'
    }

    parameters {
            snParam(credentialsForPublishedApp: "PartyReadySN", instanceForPublishedAppUrl: "", appScope: "rhino.global")
    }

    stages {
        stage('preparation') {
            steps {
                echo "${params.snParam}" // for debugging

                snApplyChanges(appSysId: "${APPSYSID}", branchName: "${BRANCH}", url: "${TESTENV}", credentialsId: "${CREDENTIALS}")
            }
        }
    }
}
