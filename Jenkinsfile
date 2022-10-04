@Library("shared-library")_
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                catchError(message:'build stage has fail blablabla',stageResult:'UNSTABLE'){
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
