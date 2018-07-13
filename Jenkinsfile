pipeline {
    agent any
    stages {
        stage("test") {
          script {
            env.BRANCHS = git ls-remote
          }
            steps {

              echo "${env.BRANCHS}"
            }
        }
    }
}
