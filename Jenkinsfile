pipeline {
    agent any

    parameters {
            snParam(credentialsForPublishedApp: "PR_GitHub", instanceForPublishedAppUrl: "https://dev104977.service-now.com", appScope: "rhino.global")
    }

    stages {
        stage('preparation') {
            steps {
                echo "${params.snParam}" // for debugging

                snApplyChanges()
            }
        }
    }
}
