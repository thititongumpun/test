pipeline {
    agent any

    triggers {
    GenericTrigger(
      genericVariables: [
      [key: 'ref', value: '$.ref']
    ],

      causeString: 'Triggered on $ref',

      token: 'Passw0rdmFec',

      printContributedVariables: true,
      printPostContent: true,
      silentResponse: false,
      regexpFilterText: '$ref',
      regexpFilterExpression: '^(refs/heads/dev)$'
    )
  }

    stages {
      stage('checkOut') {
          steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[credentialsId: '6ce24eea-09cb-4185-b631-5c288c77f2a1', url: 'git@github.com:thititongumpun/test.git']]])
          }
        }
    }
}