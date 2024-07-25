def gv

pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage("init") {
            steps {
                   echo 'init success'
                }
            }
        }
        stage("build") {
            steps {
                echo 'building application ...'
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                echo 'testing application ...'
            }
        }
        stage("deploy") {
            steps {
                echo "Deploying version ${params.VERSION}"
            }
        }
    }   
}
