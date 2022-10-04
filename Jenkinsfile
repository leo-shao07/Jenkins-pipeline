@Library("shared-library")_
pipeline {
    agent any
    environment {
        TEST_FLAG = 'false'
        DEPLOY_FLAG = 'true'
    }
    stages {
        stage('BUILD') {
            steps {
                bat "echo building......"
            }
        }
        stage('TEST') {
            when {
                environment name: 'TEST_FLAG', value: 'true'
            }
            steps {
                echo 'testing'
            }
        }
        stage('DEPLOY') {
            when {
                environment name: 'DEPLOY_FLAG', value: 'true'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
