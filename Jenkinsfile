#!/usr/bin/env groovy

node{
  checkout scm
  //def List branchs_choices = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"

    stage("test") {
      script{
        def gitURL = "git ls-remote --heads https://github.com/mbarina/testtag.git"
        def command = "git ls-remote --heads $gitURL"

        def proc = command.execute()
        proc.waitFor()

        if ( proc.exitValue() != 0 ) {
           println "Error, ${proc.err.text}"
           System.exit(-1)
        }
        println proc.getClass()

      }//script
    }//stage
}
