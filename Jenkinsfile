#!/usr/bin/env groovy

node {
    checkout scm
    stage("test") {
          //def branchs_choices = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
         //branch = input message: 'Choose branch!', ok: 'SET', parameters: [choice(name: 'BRANCH_NAME', choices: "${branchs_choices}", description: 'ciao'),]
          //echo "branch selected: {$branch}"
          try {
            timeout(time: 60, unit: 'SECONDS'){
              def sel_env =  input  message: 'Choose enviroment!',
                                    ok: 'SET',
                                    parameters:
                                      [choice(name: 'Testing', choices: 'Testing', description: 'Testing'),
                                       choice(name: 'Staging', choices: 'Staging', description: 'Staging')
                                      ]
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
