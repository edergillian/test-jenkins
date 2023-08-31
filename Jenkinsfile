pipeline {
    agent any
    BRANCH_CHOICES = ['main']
    parameters {
        choice(name: 'branch', choices: BRANCH_CHOICES, description: 'Pick a branch to build')
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
