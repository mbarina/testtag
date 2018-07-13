#!/usr/bin/env groovy

node {
    checkout scm
    stage("test") {
          try {
            def branchs_choices = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
            branch = input message: 'Choose branch!', ok: 'SET', parameters: [choice(name: 'BRANCH_NAME', choices: "${branchs_choices}", description: 'ciao'),]
            echo "branch selected: {$branch}"
            timeout(time: 60, unit: 'SECONDS'){
              def sel_env =  input  message: 'Choose enviroment!',
                                    ok: 'SET',
                                    parameters:
                                      [choice(name: 'Testing', choices: ${branchs_choices}, description: 'Testing')]


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
