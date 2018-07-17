#!/usr/bin/env groovy

node{
  script{
      timeout(time: 60, unit: 'SECONDS') {
          def gitURL = "https://github.com/mbarina/testtag.git"
          def branch = sh(returnStdout: true, script: """
                          git ls-remote --head ${gitURL} | awk '{print \$2}'
                          """)
          def selBranch = input id: 'branchSel', message: 'Select branch', parameters: [choice(name: 'selbranch', choices: "${branch}", description: 'which branch choose')]
          def runEnv =  input id: 'envSel', message: 'Select environment', parameters: [choice(name: 'runenv', choices: "Testing\nStaging", description: 'which environment choose')]
          // println "first ${branch[0]}"
          println "Branch selected "+ selBranch
          println "Environment " + runEnv
      }
  }
  environment {
    ENVSEL = ${runEnv}
    BRANCHSEL = ${selBranch}

  }
  stage("build") {
    sh 'printenv'
  }
}
