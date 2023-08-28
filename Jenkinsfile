pipeline {
    agent any
    parameters {
      string(name: 'PLANET', defaultValue: 'branch', description: 'Which planet are we on?')
      string(name: 'GREETING', defaultValue: 'Main', description: 'How shall we greet?')
      string(name: 'branch', defaultValue: 'test', description: 'Ref')
    }
    triggers {
        parameterizedCron('''
            # leave spaces where you want them around the parameters. They'll be trimmed.
            # we let the build run with the default name
            * * * * * %GREETING=Main;PLANET=branch;branch=test
        ''')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.GREETING} ${params.PLANET}"
                script { currentBuild.description = "${params.GREETING} ${params.PLANET}" }
                sleep 40
            }
        }
    }
}
