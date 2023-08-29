pipeline {
    agent any
    parameters {
        gitParameter branchFilter: 'origin/main', tagFilter: 'v(7|8)*', defaultValue: 'main', name: 'branch', type: 'PT_BRANCH_TAG', sortMode: 'DESCENDING_SMART'
    }
    stages {
        stage('Hello') {
            steps {
                checkout scmGit(branches: [[name: '$branch']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/edergillian/test-jenkins']])
                echo 'Hello World'
            }
        }
    }
}
