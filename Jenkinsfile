node {
    stage('Example') {
        echo env.BRANCH_NAME
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
        }
    }
    stage('maven') {
        withMaven(
            maven: 'maven3'
            ) {
            sh "mvn clean verify"
        }
    }
}
