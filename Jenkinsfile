def BRANCH_CHOICES = ['main', 'build', 'testing']
pipeline {
    agent any
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
