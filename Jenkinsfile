@Library("shared-library")_
pipeline {
    agent any
    parameters {
        string(name: 'NAME', defaultValue: 'John', description: 'this is name field.')
        choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
    }
    stages {
        stage('Hello') {
            steps {
                hello(name:"$NAME",day:"$DAY")
                bat "echo %cd%"
                bat "echo %~dp0"
            }
        }
    }
}