pipeline {
    agent any
    parameters {
        gitParameter tagFilter: 'v*', defaultValue: 'main', name: 'branch', type: 'PT_TAG'
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
