pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                def brachs = sh(script:"git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print \$2}'")
                echo "$branchs"
                echo "done"
            }
        }
    }
}
