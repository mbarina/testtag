#!/usr/bin/env groovy

node {
    checkout scm
    stage("test") {
          try {
            def branchs_choices = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"

            timeout(time: 60, unit: 'SECONDS'){
              def sel_branch =  input  message: 'Choose enviroment!',
                                    ok: 'SET',
                                    parameters:
                                      [AutoCompleteStringParameterDefinition(
                                        name: 'Branch',
                                        defaultvalue: 'master'
                                        description: 'Choose the branch to test'
                                        displayExpression: ${branchs_choices}
                                        valueExpression: ${branchs_choices}

              echo "Branch selected ${sel_branch}"

              def envs = "Testing\nStaging"]
              def sel_env =  input  message: 'Choose enviroment!',
                                    ok: 'SET',
                                    parameters:
                                      [choice(name: 'Testing', choices: ${envs}, description: 'Testing')]



              } //timeout
          } // try
          catch(err) {
            def user = err.getCauses()[0].getUser()
              if('SYSTEM' == user.toString()) { // SYSTEM means timeout.
                   didTimeout = true
              }
              else {
                  userInput = false
                  echo "Aborted by: [${user}]"
              } //else
          } //catch error
    } //stage test
} //node
