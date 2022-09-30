pipeline {
    agent any
    parameters {
        string(name: 'NAME', defaultValue: 'John', description: 'this is name field.')
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
