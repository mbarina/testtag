#!/usr/bin/env groovy

node {
    checkout scm
    stage("test") {
          def branch = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
          echo "{$branch}"
    }
}
