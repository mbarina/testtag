pipeline {
    agent { node { label 'node2' } }
    stages {
        stage('Test') {
            steps{
              script{
                def test = sh(returnStdout: true, script: "git tag --sort version:refname | tail -1").trim()
                echo "$test"
              }
                sh "echo $BUILD_NUMBER"
                sh  "py.test -v --host=ifdadmin@192.168.10.158 --junit-xml junit.xml /test/test_myinfra.py"
            }
        }
    }
}
