pipeline {
    agent any

    stages {
        stage('checkOut') {
          checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '6ce24eea-09cb-4185-b631-5c288c77f2a1', url: 'git@github.com:thititongumpun/test.git']]])
        }
    }
}
