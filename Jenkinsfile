pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')   
    }
    parameters {
        string(name: 'NAME', defaultValue: 'Johnn', description: 'this is name field.')
        choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
    }
    stages {
        stage('Hello') {
            steps {
                bat "echo ${params.NAME} zzzyyy ${params.DAY}"
                bat "echo %cd%"
                bat "echo %~dp0"
            }
        }
    }
}
