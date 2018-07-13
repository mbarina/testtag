pipeline {
  agent any
  stages {
    stage("test") {
      steps {
        environment {
          branch = "sh(script:"git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'")"
        }
      }
    }
  }
}
