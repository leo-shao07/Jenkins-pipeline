@Library("shared-library")_
pipeline {
    agent any
//     parameters {
//         string(name: 'NAME', defaultValue: 'John', description: 'this is name field.')
//         choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
//     }
    stages {
        stage('Hello') {
            steps {
//                 hello(name:"${params.NAME}",day:"${params.DAY}")
                bat "echo ${params.null}"
            }
        }
    }
    post { 
        failure { 
            echo 'The pipeline has fail'
        }
    }
}
