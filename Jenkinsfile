#!/usr/bin/env groovy
node {
  stages {
    stage("test") {
      steps {
          branch = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
          echo "$branch"
      }
    }
  }
}
