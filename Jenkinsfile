def BRANCH_CHOICES = ['main', 'build', 'testing']
pipeline {
    agent any
    triggers {
        cron 'H/2 * * * *'
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "$env.BRANCH_NAME"
            }
        }
    }
}
