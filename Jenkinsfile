pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }
    stages {
        stage('elasticache Pipeline') {
            // when {
            //     anyOf {
            //         changeset "components/elasticache/**"
            //         changeset "terraform_modules/elasticache/**"
            //         triggeredBy cause: "UserIdCause"
            //     }
            // }
            stages {
                stage('Build elasticache') {
                    steps {
                        echo '----------------------'
                        echo "${currentBuild.buildCauses}" // same as currentBuild.getBuildCauses()
                        echo '----------------------'
                        echo "${currentBuild.getBuildCauses('hudson.model.Cause$UserIdCause')}"
                        echo '----------------------'
                        echo "${currentBuild.getBuildCauses('hudson.triggers.TimerTrigger$TimerTriggerCause')}"
                        echo '----------------------'
                        echo 'build elasticache'
                    }
                }
            }
        }
    }
}
