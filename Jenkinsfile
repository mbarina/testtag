pipeline {
    agent any
    stages {
        stage("test") {
          script {
            env.BRANCHS = git ls-remote --heads | awk '{print $2}'
          }
            steps {

              echo "${env.BRANCHS}"
            }
        }
    }
}
