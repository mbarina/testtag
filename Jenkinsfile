pipeline {
    agent any
    stages {
        stage("test") {
            steps {
              script {
                env.BRANCHS = git ls-remote
              }
              echo "${env.BRANCHS}"
            }
        }
    }
}
