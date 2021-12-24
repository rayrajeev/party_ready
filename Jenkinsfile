pipeline {
    agent any

    parameters {
            snParam(credentialsForPublishedApp: "88dbbe69-0e00-4dd5-838b-2fbd8dfedeb4", instanceForPublishedAppUrl: "https://dev104977.service-now.com", appScope: "")
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
