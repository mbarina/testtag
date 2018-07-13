pipeline {
    agent any
    stages {
        stage("test") {
              BRANCHS = sh(script:"git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'")
              echo ${BRANCHS}
        }
    }
}
