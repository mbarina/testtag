pipeline {
    agent any
    stages {
        stage("test") {
                  sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print $2}'"
                  echo ${BRANCHS}
        }
    }
}
