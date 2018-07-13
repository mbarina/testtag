#!/usr/bin/env groovy
node {
    stage("test") {
      step {
          branch = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
          echo "$branch"
      }
    }
}
