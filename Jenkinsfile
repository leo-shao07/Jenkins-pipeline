@Library("shared-library")_
pipeline {
    agent any
    parameters {
        string(name: 'NAME', defaultValue: 'John', description: 'this is name field.')
        choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
    }
    stages {
        stage('Build') {
            steps {
                catcherror(message:'build stage has fail blablabla'){
                    bat "exit 1"
                }
            }
        }
        stage('Test') {
            steps {
                bat "echo this is Test stage"
            }
        }
    }
}
