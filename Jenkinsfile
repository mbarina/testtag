pipeline {
    agent any
    stages {
        stage("test") {

            steps {
              script {
                env.BRANCHS = sh "git ls-remote --heads | awk '{print $2}'"              }
              }
              echo "${env.BRANCHS}"
            }
        }
    }
}
