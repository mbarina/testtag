pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                  sh "git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print $2}'"
                  echo ${BRANCHS}
            }
        }
    }
}
