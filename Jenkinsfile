@Library("shared-library")_
pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')   
    }
    parameters {
        string(name: 'NAME', defaultValue: 'John', description: 'this is name field.')
        choice(name: 'DAY', choices:["Mon","Tue","Wed"],description: "select week days")
    }
    stages {
        stage('Hello') {
            steps {
                hello(name:"${params.NAME}",day:"${params.DAY}")
                addSidebarLink(url:'https://www.trendmicro.com/zh_tw/forHome.html', text:'Trendmicro website', icon:'/userContent/icon.png')
                bat "echo %cd%"
                bat "echo %~dp0"
            }
        }
    }
}
