pipeline {
    agent any
    parameters {
      string(name: 'PLANET', defaultValue: 'branch', description: 'Which planet are we on?')
      string(name: 'GREETING', defaultValue: 'Main', description: 'How shall we greet?')
      gitParameter(tagFilter: 'v\* main', defaultValue: 'main', name: 'tag', type: 'PT_TAG')
    }
    stages {
        stage('Example') {
            steps {
                git url: 'https://github.com/edergillian/test-jenkins'
                echo "${params.GREETING} ${params.PLANET}"
                script { currentBuild.description = "${params.GREETING} ${params.PLANET}" }
                sleep 40
            }
        }
    }
}
