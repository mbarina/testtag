#!/usr/bin/env groovy

node {
    checkout scm
    stage("test") {
          // try {


            //timeout(time: 60, unit: 'SECONDS'){

            script{
              boolean isCollectionOrArray(object) {
                  [Collection, Object[]].any { it.isAssignableFrom(object.getClass()) }
              }
              def String str = ''
                 // for(String item: branchs_choices){
                 //   sh "echo ${item}"
                // }
              def branchs_choices = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
              def result = branchs_choices.getClass()
              isCollectionOrArray(branchs_choices)
              sh "echo ${result}"
               //
               //
               // for (int i = 0; i < branchs_choices.size(); i++){
               //    str += '\n' + branchs_choices[i]
               //
               // }

               //sh "echo ${str}"
            }
             //}
              // def sel_branch =  input  message: 'Choose enviroment!',
              //                       ok: 'SET',
              //                       parameters:
              //                         [AutoCompleteStringParameterDefinition(
              //                           name: 'Branch',
              //                           defaultvalue: 'master',
              //                           description: 'Choose the branch to test',
              //                           displayExpression: '${branchs_choices}',
              //                           valueExpression: '${branchs_choices}'
              //                           )]
              //
              //
              //
              // def envs = "Testing\nStaging"
              // def sel_env =  input  message: 'Choose enviroment!',
              //                       ok: 'SET',
              //                       parameters:
              //                         [choice(name: 'Testing',
              //                                 choices: '${envs}',
              //                                 description: 'Testing')
                                      // ]

              //} //timeout
          // } // try
          // catch(err) {
          //   def user = err.getCauses()[0].getUser()
          //     if('SYSTEM' == user.toString()) { // SYSTEM means timeout.
          //          didTimeout = true
          //     }
          //     else {
          //         userInput = false
          //         echo "Aborted by: [${user}]"
          //     } //else
          // } //catch error
    } //stage test
} //node
