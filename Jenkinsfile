pipeline {
    agent any
    stages {
        stage("test") {
            steps {
              script {
                  env.BRANCHS = git ls-remote --heads | awk '{print $2}'
              }
              echo "${env.BRANCHS}"
            }
        }
    }
}
