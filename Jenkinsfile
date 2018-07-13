#!/usr/bin/env groovy
pipeline {
  agent any
  stages {
    stage("test") {
      steps {
          branch = sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'"
          echo "$branch"
        }
      }
    }
  }
}
