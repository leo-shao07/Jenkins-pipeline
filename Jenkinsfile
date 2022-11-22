@Library("shared-library")_
pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '3', daysToKeepStr: '', numToKeepStr: '5')   
    }
    parameters {
        string(name: 'NAME', defaultValue: 'Johnn', description: 'this is name field.')
        choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
    }
    stages {
        stage('Hello') {
            steps {
                hello4mac(name:"${params.NAME}",day:"${params.DAY}")                
            }
        }
    }
}
