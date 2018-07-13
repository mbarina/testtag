pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                  env.BRANCHS = git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print $2}'
                  echo "${env.BRANCHS}"
                }
            }
        }
    }
}
